golang ��xml�����

dom4g�ṩxml���Ĳ�����������ڵ� ���ӣ�ɾ������ѯ���������ӣ��޸ģ�ɾ������ѯ�ȹ���

����������Լ������ļ�dom_test.go

func TestAdd(t *testing.T) {
	fmt.Println()
	fmt.Println("-------------------------TestAdd-----------------------------")
	s := `<a Age="10"><d>dong</d><d>wxd</d><e><f>hello</f></e></a>`
	el, _ := LoadByXml(s)
	el.AddNodeByString(`<h>���</h>`)              //�����ڵ��������Ϊ�ַ���
	el.AddNode(&Element{Name: "g", Value: "����"}) //�����ڵ����ΪElement
	fmt.Println(el.ToString()) 
	//����̨��ӡ
	//<a Age="10"><d>dong</d><d>wxd</d><e><f>hello</f></e><h>���</h><g>����</g></a>
}