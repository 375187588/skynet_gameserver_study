--create by NaiveBug^����
��ʼǰ׼��
1:��װMysql,��������û���:iphone,����:iphoneGame (�����Լ��޸�mysql/sql�µ�����)
2:����sql��sql.sql�����ݿ�,֮����startkt.bat��skynet.exe����������Ϸ������
--
˵��:
1������ΪSkynet�߼�ѧϰ����,��exeִ���ļ�����Skynet�����ǹٷ��汾Window�������ؿ����б���,�����ҵ��;�Լ���Linuxȥ��,�����ƽ̨����һ���ǿ��õ�.
2������code/scrpit��,����ΪSkynetԭ������..
--
������:(����Ҫ������Skynet������Ӵ���)
1ÿ�����һ��Agent,�ͻ��˷�������ת��Agent���netcommon.netPackCommon�ɷ�������Ϣ,Ȼ��ת��net�µ�netcommon.netPackCommon���ÿ�������������,����򵥿ɿ�netchat
2whoΪplayer,��GetPlayer()��ȡ
3����Э����뷽ʽ��Protobuf,�ͻ�������Կ�google��Protobuf,Skyenet���õ����Ʒ����c���԰��protobuf,Э������protos��,pb�ļ����ɷ�ʽ�Լ��Ѱٶ�~protobufinit��ʼ���ͼ���protobuf
4�üǵ�¼����netbase.C2SLogin�½���ִ�н��뵽account���LoadPlayerData�����������,���ݼ��غͲ�����Ҫ��player��m_DBList��m_WhenUpdateSaveList�б�,(m_WhenUpdateSaveList�и���ʱ�Ż���һ��ʱ��洢,���򲻴洢)
5m_DBList��m_WhenUpdateSaveList������������Ҫ�Ķ���֮һ�������洢����,������db��dbmgr��
6dataΪ��������,�������ɵķ�ʽ�ɿ����˵�pyhton_read_excel_to_lua�������,data/share.lua��ʼ����������,��������Ϊ�˽�ʡ�ڴ�,����ÿ�������������һ��,ֻҪ�������õ��ļ���..ʹ��skyent��sharedataʵ��
7npc�����ֺܶ����ݵĴ洢��ʽ����herodb�µ�load��save,����ʱ��dbmgr�µ�load��save���ò���.����ͨ��g_pickle.serializeTable���л����ַ����浽Mysql,
8���ݴ洢���Ի������ݲ������Կ�ļ����ַ�������ʽ�浽���ݿ�ͼ���ʹ��.���Է�װ�ú�,�������ϲ�д�߼�,�����ù��������洢����~��Ϊ��player��AutoSave�����Ӷ�ʱ�ص�Saveȥ�������ݿ����Ƿ��и���,�вŴ�,
9�����Ƿ���µ��õ���UpdateSave�������~����õ�herodb��CheckUpdate���ÿ�������Ƿ��и���,��ÿ��Chero�̳�base/only�µ�DictKeysCtrl��CDictKeysCtrl��IsUpdate����,������д���ʱ�򾡹���Set��Query����table���ݼ���,��Chero:SetName��Chero:GetName()�������..��ֻҪ�����˾ͻ��Զ��洢���Զ�����,Ҳ���ǵ��˲��ù������ݵĵز�,�ǳ��ǳ��ķ���ͷǳ��Ŀ�ݿ���...
10:BaseClass(CNpc)����д��ķ�ʽ����base/BaseClass��д��,���Ʒ�06��д��Lua��,��ֻ��NPC���ֶ�������ʵ������,Ϊ�˽�ʡ�����ڴ�,��ʵҲ���Բ���,ֱ����createdbmgr�������ɷ�ʽҲ����,����ͳһʹ��self.xx������self:xx~~
-------------------------finsh----------------
�кν���������������ۻ�SkynetȺ��@clear,�Ʒ���������������,������������С����...