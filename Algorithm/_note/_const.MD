/*****************************************************************
	
*****************************************************************/
/// 
/// http://lib.csdn.net/article/cplusplus/30981
///

	const������������˼�壬���ǲ��ܸı�ĵ��������ǳ���������������const�����ġ�
	����˵������������һ��const��������
	[cpp] view plaincopy
					vector<int> vv(10,9);  
					const vector<int> :: iterator iter = vv.begin();  
	�򣬵������г������������ʱ�Ǵ����

	[cpp] view plaincopy
					++iter;  

	��ԭ����iter��һ������������ǲ��ܸı�ġ�
	���仰˵��iterֻ��ָ��vv�ĵ�һ��Ԫ�أ�����ָ��������Ԫ�ء�
	�����������������ȷ�ģ�

	[cpp] view plaincopy
					��iter = 10;  

	��Ϊ��Ȼiter����ָ��������Ԫ�أ�������ָ��ĵ�һ��Ԫ�ص�ֵ�ǿ��Ըı�ġ�
	������const_iterator��˵�Ļ��������෴������������������

	[cpp] view plaincopy
					vector<int> vv(10,9);  
					vector<int> :: const_iterator iter;  

	��������һ��const_iterator��������
	����������ǿ����Լ����ӵģ���������ָ���Ԫ���ǲ����Ա��ı�ġ�
	����˵

	[cpp] view plaincopy
					for(iter = vv.begin(); iter != vv.end(); ++iter){  
						cout << *iter << endl;  
					}  

	��������ȷ�ģ���iter������ֵ�ǿ��Ըı�ġ�����

	[cpp] view plaincopy
					for(iter = vv.begin(); iter != vv.end(); ++ iter){  
					   *iter = 0;  
					}  

	�����ǲ��Եģ���Ϊconst_iterator�������ǲ��ܸı�����ָ���Ԫ�ص�ֵ�ġ�