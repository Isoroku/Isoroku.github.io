---
marp: true
theme: A4-Manual
header: "__BACnet-GW__"
#footer: "by yamamoto.matsuki.cmc��osaka-u.ac.jp-makes**"
---
  <div class="top"><p class="size12">�y�閧�z �֌W�ҊO�� </p></div>



<div class="center">
##### BACnet-GW�̗v���d�l���i0.32�Łj <br>  
<p class="size16">�iCOV�ʒm�@�\�E�|�[�����O�@�\�ǉ��j</p>
</div>



<div class="center">
  <p class="size12">
  �ߘa7�N2��28��<br>  
  ������w�@�l����wD�R�Z���^�[<br>  
  ����������
  </p>
</div>







---
<div class="size14">

�ڎ�[���R1]
1	�T�v	2
1.1	�w�i�E�ړI	2
1.2	�V�X�e���\���}	2
2	�{�d�l���ŊJ������V�X�e���̍\���T�v	3
2.1	BACNET�Ǘ��@�\	3
2.2	BACNET-WOT�ϊ��@�\	4
2.3	COV�ʒm�@�\	5
2.4	ADT�A�g�@�\	6
3	�@�\�v��	6
3.1	BACNET�Ǘ��@�\	6
3.1.1	BACnet�f�o�C�X�T���@�\�i�}�Q�@�@�\?@�j	6
3.1.2	BACnet�f�o�C�X�̊�{���̎擾�E�ۑ��@�\�i�}�Q�@�@�\?A?B�j	6
3.1.3	BACnet�f�o�C�X�̌��ݒl���̎擾�E�ۑ��@�\�i�}�Q�@�@�\?C�j	10
3.1.4	����f�o�C�X�̌��ݒl�v���p�e�B�̍X�V�@�\�i�}�Q�@�@�\?D�j	10
3.1.5	API�T�[�o�@�\�i�}�Q�@�@�\?E�j	10
3.1.6	COV�Ǘ����W���[�������COV�ʒm����M�^���M�y�уf�[�^�̓������@�\	11
3.2	BACNET-WOT�ϊ��@�\	11
3.2.1	�o�^�f�o�C�X�̏��̎擾�@�\	15
3.2.2	�f�o�C�X�̐U�镑�����`����V���O��`�@�\	15
3.2.3	�����f�[�^�]���@�\�y�񓯊��ʐM����������Event�@�\	17
3.2.4	�e�V���O��������WOT�T�[�o���J�n����@�\	19
3.2.5	�o�^�f�o�C�X���̊Ď��@�\	20
3.2.6	COV�Ǘ����W���[�������COV�ʒm����M�y�ё��M����@�\	20
3.3	ID�ϊ��@�\	21
3.3.1	�f�[�^�[�x�[�X�̍\��	21
3.3.2	�f�[�^�[�x�[�X����@�\	22
3.4	COV�ʒm�@�\	24
3.4.1	�f�o�C�X���擾�@�\	24
3.4.2	���M�E��M�@�\	24
3.4.3	�o�^���擾�@�\	24
3.4.4	�o�^/�����@�\	25
3.4.5	COV�ʒm�@�\	27
3.4.6	���̑�COV�Ǘ��T�[�o�[�̋@�\	27
3.5	AZURE DIGITAL TWINS�A�g�@�\	29

</div>
---
<div class="size14">
3.5.1	HTTP�v���g�R���ɂ�������	29
(1)	�v�b�V���^�̑��M�N���C�A���g�@�\	29
(2)	�A�g�@�\�𐧌䂷��T�[�o�[�@�\	29
3.5.2	MQTT�v���g�R���ɂ�������	30
(1)	PUB�T�[�o�[�@�\�i�N���C�A���g�@�\�܂ށj�iBACnet-GW�j	30
(2)	MQTT�N���C�A���g�@�\�i�Ď��N���C�A���g�F�r��OS�܂ށj	30
3.5.3	COV�ʒm�@�\��z�肵��������	32
4	�J����	33
4.1	BACNET�Ǘ��@�\	33
4.2	BACNET-WOT�ϊ��@�\	34
4.3 ���s��	35
4.4�Q�l	36
4.4.1 BACnet�Ή�CO�Q�Z���T�[�̎���	36
4.4.2 BACnet�̊e�d�l��`	36
4.4.3 �t�@���R�C���G�~�����[�^�̎����i�]���p�j	37
4.4.4 WOT���Ɍ�����BACnet�̎d�l�̌���	37

</div>
---

#### 1. �T�v

<div class="size14">
1. �w�i�E�ړI  
�@����܂ŁA�_�C�L���H�Ƃ̒񋟂���󒲊֘A��API��Ղł���DK-CONNECT��p���āA�󒲃f�o�C�X��WOT(Web of Things)���𐄐i���AW3C�̕W���K�i�ɑ���e�󒲋@�փA�N�Z�X���邽�߂̕��@�_��W�J���Ă����B���ɑO�N�x�́A���̉��p�̈�Ƃ���WOT�Ƃ��ĔF�����ꂽ�e�󒲃f�o�C�X���AAzure�f�W�^���c�C���ƘA�g����d�g�݂��āA�\�z���Ă����B
�@2023�N�x�́A��N�x�̐��ʂ𔭓W�����ADK-CONNECT�ȊO�̑��Ћ@��/�ݔ����r��OS�ɐڑ�����ۂɍX�ɁA�g���₷���V�X�e���̊J����ڎw���B���ɁA�r���̓����I�ȊǗ��V�X�e���ł���A������f�t�@�N�g�X�^���_�[�h�ƂȂ��Ă���BACnet�Ƃ̐ڑ������������邱�Ƃɂ��A���Аڑ��Ɍ����X�ɁA�_��V�[�����X�ȃV�X�e���̍\�z�����҂ł���B  

1. �V�X�e���\���}
�@�}�P�ɖ{�V�X�e���̑S�̍\���������B�Ԑ��̘g�����{�V�X�e���͈̔͂ł���B�{�V�X�e���̑O��Ƃ��ẮA�}�ɂ���ʂ�]���̒����Ď����u��u�������邱�Ƃł͂Ȃ��A�������񂵂ăr������BACnet�f�o�C�X�̏����r��OS�ɒ񋟂��邱�Ƃ�z�肷��B���Ȃ킿�A�r�����̊e�@��́i�~�b�V�����N���e�B�J���ȁj�Ď��E����͏]���̒����Ď����u���S���Ă��邱�Ƃ�O��ɁA�����Ɋe�@��̏������W���A�r��OS��Ƀr���̃f�W�^���c�C�����\�z���邱�ƂŁA�V���ȕt�����l���������r���A�v���P�[�V�����̎������\�Ƃ��邱�Ƃ�ړI�Ƃ���B���������āA�{BACnet GW�ɂ����ẮA�r�����̊e�@��̐�����s�����Ƃ�ے�͂��Ȃ����A��Ȗ����Ƃ��Ă̓f�[�^�̎��W�ɂ�����̂Ƃ���B
�@�{BACnet-GW�͐}1�ɂ���ʂ�ABACnet�f�o�C�X�Ǘ��T�[�o�@�\��BACnet-WoT�ϊ��T�[�o�@�\�ɉ�����ADT�iAzure Digital Twin�j�A�g�@�\�ō\�������B�����͕����I�ɂR��̃T�[�o�i�N���C�A���g���܂ށj�ō\�������Ƃ������Ƃ��Ӑ}������̂ł͂Ȃ��ABACnet-GW�������̂R�̋@�\���W���[���������Ƃ��Ӑ}�������̂ł���B

![alt text](image.png)

�y�}1�z�@��������BACnet�ɂ��r���Ǘ��V�X�e���̃l�b�g���[�N�C���[�W

</div">

#### 2. �{�d�l���ŊJ������V�X�e���̍\���T�v

<div class="size14">
�}�Q�ɖ{�V�X�e���̋@�\�T�v�������B

1.  BACnet�Ǘ��@�\
�ȉ��̂V�̋@�\�ō\�������
    1. �f�o�C�X�̒T���@�\
    2. �擾�����f�o�C�X�̊�{���̎擾�@�\
    3. ��L�擾����DB�ւ̕ۑ��@�\
    4. �e�f�o�C�X�̌o���I�ω��̂�����̎擾�@�\
    5. ����f�o�C�X�̌��ݒl�v���p�e�B�̍X�V�@�\
    6. �eBACnet�f�o�C�X�̏��擾�܂��́A�f�o�C�X��������s���邽�߂�API�T�[�o�[�@�\
    7. COV�Ǘ����W���[�������COV�ʒm����M�^���M�y�уf�[�^�̓������@�\

![alt text](image-1.png)


�y�}2�z�@BACnet-WOT�ϊ��V�X�e���̍\���}


---
2. BACnet-WOT�ϊ��@�\
�@�ȉ���7�̋@�\�ō\�������
  1. BACnet�f�o�C�X�Ǘ��T�[�o�������I�ɓo�^�f�o�C�X�̏��̎擾�@�\
  1. �擾�����f�o�C�X�̃v���p�e�B�������Ƀf�o�C�X�̐U�镑�����`����V���O�̃e���v���[�g�̍쐬�@�\
  1. �e�V���O��������WOT�T�[�o���J�n����@�\�iWOT�T�[�o�[�̍ċN���́A����p���z�V���O��p���ăL�b�N����j
  1. �eWOT�T�[�o�́ABACnet�f�o�C�X�Ǘ��T�[�o��API����ăf�o�C�X�̍ŐV�����|�[�����O���ăV���O�Ƃ̓��������s���@�\
  1. �f�o�C�X�o�^���̊Ď��̌��ʁA�o�^�f�o�C�X���ɕύX�i�ǉ��E�폜�j���������Ƃ��ɊǗ��҂��č\���L���𔻒f���A���݂�WOT�T�[�o���~�����A�ēx�V�����\���Ƃ���WOT�̃T�[�r�X���J�n����@�\
  1. COV�Ǘ����W���[�������COV�ʒm����M�y�ё��M����@�\
  1. COV�ʒm�ɂ��f�[�^�������y�у����O�|�[�����O�����@�\


- COV�ʒm�@�\
�W�L�@�\�́A�ǉ��̃I�v�V�����@�\�Ƃ��č\�������B
�}�R��COV�ʒm�@�\�iCOV�Ǘ����W���[���j��ǉ������ꍇ�̍\���}�������B
![alt text](image-2.png)

�y�}�R�z�@COV�Ǘ����W���[����ǉ������S�̂̃V�X�e���̍\����
�@�ȉ��̂T�̋@�\�ō\�������
1. �f�o�C�X���擾�@�\
1. WebSocket��p�������M�E��M�@�\
1. �o�^���擾�@�\
1. �o�^/�����@�\
1. COV�ʒm�@�\


- ADT�A�g�@�\
�@�ȉ��̂T�̋@�\�ō\�������
?@ BACnet-WOT�ϊ��@�\�������I�ɊeWOT�̃v���p�e�B�l���擾����@�\
?A WOT�̃v���p�e�B�l�ɕύX�������ADT���ŋK�肳�ꂽ�t�H�[�}�b�g�ɕϊ�����@�\
?B ADT�ւ̃A�N�Z�X�ɕK�v�ȃg�[�N����F�؃T�[�o�[����擾����@�\
?C ��L�A�N�Z�X�g�[�N����?A�ō쐬�����f�[�^�ɕt�^���ăW�^���c�C���֑��M����N���C�A���g�@�\
?D ADT���܂ފO���N���C�A���g����̃��N�G�X�g�ɉ����ĉ�������T�[�o�[�@�\�B��̓I�ȃT�[�o�[�@�\�Ƃ��ẮA�f�W�^���c�C���ւ̑��M�J�n�A��~�y�сA�X�V�Ԋu�ݒ�@�\���܂ށB
?E WOT�ϊ��T�[�o�[�Ƀ����O�|�[�����O���s�������f�[�^�Ɋ�Â�PATCH��������@�\


</div>
---
#### 3. �@�\�v��

<div class="size14">
�@�ȉ��A�e�߂Ŋe�@�\�v�f�̋@�\�ŏ�L�̎d�l���������B�ȉ��A����V�K�J������@�\�ɂ��ďq�ׂ�B
�@
	1. BACnet�Ǘ��@�\
		1. BACnet�f�o�C�X�T���@�\�i�}�Q�@�@�\?@�j  

* BACnet�f�o�C�X�Ɏ�������Ă���Discovery�T�[�r�X�iWho-Is/I-am�j�@�\��p���āA�z���ɂ���f�o�C�X���𔭌����A�f�[�^�[�x�[�X�ɓo�^����B��莞�Ԃ��Ƃɓ��삳���邱�Ƃɂ��ŐV�̏���ێ�������̂Ƃ���B�z��f�o�C�X���́A100����x�Ƃ��āAB-BC�P�ʂ��Ƃɔz�u���邱�ƂƂ���B�V�K�o�^�́A�ݒ�t�@�C���ɂ��w�肷�邩�AAPI������ݒ�ύX���\�Ƃ���B

		1. BACnet�f�o�C�X�̊�{���̎擾�E�ۑ��@�\�i�}�Q�@�@�\?A?B�j
* �f�o�C�X�������W���邽�߂�BACnet�̊�{�T�[�r�XRead Property�T�[�r�X���g�p����B�����āA���W�����f�o�C�X�������ƂɁA�e�f�o�C�X�̃I�u�W�F�N�g�y�уv���p�e�B�����Ǘ����Ƃ��ĕۑ�����B
* �e�f�o�C�X�̏��́A�ύX�p�x�������Ȃ��v���p�e�B���i�f�o�C�X�ŗL�j�́A�f�[�^�[�x�[�X���Ɋi�[����B�i��F�I�u�W�F�N�g���A�v���l�̍ő�l��ŏ��l�y�ьv���l�̒P�ʂȂǁj
* BACnet�f�o�C�X��Identifier�͈̔͂��w�肵�āA�O���[�v�P�ʂŊǗ��ł���悤�ɂ���B
* �t�B�[���h���̊��݂̃V�X�e���ɉ�����BACnet�f�o�C�X��Identifier�����O�ɂ킩��Ȃ��ꍇ��z�肵�āA���������f�o�C�X�������I�ɓo�^���邵���݂��l�����Ă����B

�y�\3-1�z�@BACnet�Ǘ��T�[�o�ݒ�t�@�C���i����C�Ή������Łj ver.0.5.4
����
�L�[
�ݒ�l�i��j
Who-Is���s�Ԋu
whois_interval
Default: 60�b
���ݒl�̍X�V�p�x
update_interval
Default: 30�b < Who-Is���s�Ԋu
�����������
window_size
Default: 5��
�O���[�v�Ǘ��p�f�o�C�XId��
group_ids
Default: �Ȃ�(0�`4194303)�˕�����
�����o�^�̎��F['*']
�T�[�o�|�[�g�ԍ�
port
Default: 5000
�T�[�o�[�A�h���X
addr
�l�b�g�}�X�N��IP�A�h���X("172.16.0.123/16")
BACnet�|�[�g
bacn_port
47808
�����o�^���[�h���̍ő�f�o�C�XId
max_ids
Default: 0
�����o�^�̎��ɐݒ肷��B0�l�̎��ɍő�l�Ƃ���B
�ΏۂƂ���I�u�W�F�N�g�^
object_list
�I�u�W�F�N�g�^�̔z��
�}���`�v��READ���Ή��f�o�C�X�̎w��
multiple_unsupported
�@Default:[] �iex: ["11"]�j
�}���`�v��READ�Ή��f�o�C�X�̍ő�v���p�e�B���̎w��
multiple_n_partitions
Default: 100
READ�ΏۃI�u�W�F�N�g�w��t�@�C����
alive_list
Default: ""

(��̗�)
�ݒ�t�@�C���F config_v1.json
{
  "whois_interval": 60, 
  "update_interval": 30, 
  "window_size": 5, 
  "port": 5001,
  "addr": "192.168.100.4/24",
  "bacn_port": 47808,
  "group_ids": ["11", "5001-5010"],
  "max_ids": 0,
  "object_list": ["analogInput", "analogOutput", "analogValue", "binaryInput", "binaryOutput",
    "binaryValue", "multiStateValue", "multiStateInput'", "multiStateOutput", "device"],
  "multiple_unsupported": ["11"],
  "multiple_n_partitions": 100,
  "alive_list": " "alive_demo,json""
}

�ΏۃI�u�W�F�N�g�w��t�@�C��
�ȉ��̃I�u�W�F�N�g�\���Ƃ���B
�L�[�F�@�f�o�C�XID
�l�F�@�I�u�W�F�N�gID�̃��X�g
��̗�͈ȉ��̂Ƃ���B�t�@�C�����Falive_demo.json


�y�\3-1a�z�@BACnet�Ǘ��T�[�o�ݒ�t�@�C���i����C�Ή������Łj ver.0.6.7
����
�L�[
�ݒ�l�i��j
Who-Is���s�Ԋu
whois_interval
Default: 60�b
���ݒl�̍X�V�p�x
update_interval
Default: 30�b < Who-Is���s�Ԋu
�����������
window_size
Default: 5��
�O���[�v�Ǘ��p�f�o�C�XId��
group_ids
Default: �Ȃ�(0�`4194303)�˕�����
�����o�^�̎��F['*']
�T�[�o�|�[�g�ԍ�
port
Default: 5000
�T�[�o�[�A�h���X
addr
�l�b�g�}�X�N��IP�A�h���X("172.16.0.123/16")
BACnet�|�[�g
bacn_port
47808
�����o�^���[�h���̍ő�f�o�C�XId
max_ids
Default: 0
�����o�^�̎��ɐݒ肷��B0�l�̎��ɍő�l�Ƃ���B
�ΏۂƂ���I�u�W�F�N�g�^
object_list
�I�u�W�F�N�g�^�̔z��
�}���`�v��READ���Ή��f�o�C�X�̎w��
multiple_unsupported
�@Default:[] �iex: ["11"]�j
�}���`�v��READ�Ή��f�o�C�X�̍ő�v���p�e�B���̎w��
multiple_n_partitions
Default: 100
READ�ΏۃI�u�W�F�N�g�w��t�@�C����
alive_list
alive_list_minho.json
�I�u�W�F�N�g�̃|�[�����O�w����`�t�@�C����
interval_list
interaval_def.json


�i��j�@interval_def.json

---
3.1.3 BACnet�f�o�C�X�̌��ݒl���̎擾�E�ۑ��@�\�i�}�Q�@�@�\?C�j
�@���ݒl�Ȃǌo���I�ɕω�����v���p�e�B�́A�|�[�����O�ɂ�胁�����[��ɕۑ����邱�ƂƂ���B
�f�[�^�X�V�̃|�[�����O���Ԃ́A��{�^�C���X���b�g���Ԃ��x�[�X�ɁA���̐����{�Ƃ��ĔC�ӂɐݒ�\�Ƃ���B�Ȃ��A�e�I�u�W�F�N�g���̐ݒu���l�X�ȏ�ʂł̉��p���l�����Ēǉ�����B�����v���p�x�́A�����ݒ�t�@�C���Ŏw�肷�邱�ƂƂ���B�܂��A�v���p�x�́AAPI�@�\�Ɍv���p�x�ύX�T�[�r�X���쐬���邱�Ƃɂ��^�p���ɍX�V�\�Ƃ���\��ł���B
�@Property�̓ǂݏo���́A3�D1�D2���l�ɁA��{�I��Read Property�T�[�r�X�ɂ���������B�܂��A�擾�̌������ɑ΂���Read Property Multiple�T�[�r�X���K�v�ɉ����Ēǉ�����BCOV�T�[�r�X�Ɋւ��ẮA�{�d�l���ɂ����Ă̓X�R�[�v�O�Ƃ���B
�@
�@�ȉ��͖{�d�l���ɂ����鐫�\�v���̌��ς���ł���B�����ł͐��\�v���Ƃ��āA1[min]���Ƃ̃f�[�^�̎擾��z�肵�A���l�̃f�o�C�X��100�Ԃ牺����Ɖ��肷��B�ȉ�100�̃f�o�C�X�̑S�v���p�e�B���擾���鎞�Ԃ����ς���B
�@1[min]���Ƃ̗v����O��ɂ���ƁA60[sec]�ȓ��ɂ́A�S�Ẵf�o�C�X�̌��ݒl���X�V����K�v�����邪�A�]�T���݂�30[sec]���ƂɍX�V���s���B
�@1�̃f�o�C�X�����苖�e�����擾���ԁ@=�@30[sec]/100 = 300 [msec] 
�@�]���āA300[msec]�ȓ��ɂP�f�o�C�X���ێ����邷�ׂẴI�u�W�F�N�g�̌��ݒl���擾����K�v������B�Ⴆ�΁A���݂�CO2�Z���T�̑ΏۃI�u�W�F�N�g�͂T���݂��Ă���A�����_�̕]���ł͂��̗v���͖������Ă���B���݂̎����ł́A�S�f�o�C�X����V���A���ɓǂݎ����s���Ă��邪�A�ڑ��䐔��ǂݎ��Ԋu�Ȃǂ̗v����ABACnet-GW����������f�o�C�X�̐��\�Ȃǂɂ���āA�p�������ɓǂݎ����s���Ȃǂ̕ύX���K�v�ɂȂ�\��������B

�@�ȏォ��A�ڕW�l�͕\3-2�̂Ƃ���Ƃ���B
�@
�@
�y�\3-2�z
����
�ڕW�l
BACnet�I�u�W�F�N�g��
�S�I�u�W�F�N�g����10,000���x
���ݒl�̍X�V�p�x
5�b�ȏ�A�C�ӂɐݒ�\�Ƃ���
���ݒl�̎擾����
�ő�300msec����(1�f�o�C�X������)?


---
3.1.4 �|�[�����O�X�P�W���[���@�\�i�}�Q�@�@�\?C�j
�@��{�^�C���X���b�g���Ԃ��x�[�X�ɂ��̐����{�Ƃ��Ē�`�����|�[�����O�Ԋu�ɂ����āA�e�I�u�W�F�N�g�̃v���p�e�B���ǂ̃^�C���X���b�g�Ŏ擾���邩�����肷��ȉ��̃��[�h��݂���B

?@  �P���ȊԈ������[�h
�{���[�h�́A�Ԉ��������̕W�����[�h�̊܂ށB
?A ���Srandomize���[�h
��L?@�ŒP���ɊԈ����ƁA�e�^�C���X���b�g���Ɋ��蓖�Ă��擾�I�u�W�F�N�g�̐��Ƀo���c�L�������邽�߂ɁA�^�C���X���b�g���̃f�[�^���N�G�X�g������сA���̃f�[�^�擾���ԂɃo���c�L�������Ă��܂��B���̂��߂Ƀ^�C���X���b�g���Ɋ��蓖�Ă�I�u�W�F�N�g�����������ł���悤�Ɉ�l������p���ăX�P�W���[������d�l�Ƃ���B
?B ����randomize���[�h
��L?A�̃��[�h�ƈقȂ�̂́A�f�o�C�X���œ��������Ńf�[�^�擾����I�u�W�F�N�g�i�v���p�e�B�j�̃^�C�~���O�𓯂��^�C���X���b�g���Ɏ��߂�_�ł���B

�y�\ 3-3�z�@�e���[�h�ƃ��[�h�w�W�Ƃ̊֌W�\
mode
����
0
�P���ȊԈ������[�h
1
���Srandomize���[�h
2
����randomize���[�h�i�f�o�C�X���ōS���j


3.1.5 ����f�o�C�X�̌��ݒl�v���p�e�B�̍X�V�@�\�i�}�Q�@�@�\?D�j

�@����f�o�C�X�̃v���p�e�B�l���X�V���邽�߂�BACnet��Write Property�T�[�r�X���������Ď�������B��̓I�ȑz��C���[�W�́AWOT������̐ݒ�l�ύX��R�}���h�̔��o�ɔ���BACnet�f�o�C�X�ɑ΂��Ă����̃R�}���h�����s���邱�ƂƂ���B

3.1.6 API�T�[�o�@�\�i�}�Q�@�@�\?E�j
�@�e�f�o�C�X�̏��܂��́A�f�o�C�X����́AAPI�@�\���������邱�Ƃɂ���������B�Ⴆ�΁A�e�f�o�C�X�̌��ݒl���ł���΁A��������̊Y���f�[�^�𒊏o���ă��N�G�X�g�ɉ������邱�ƂƂ���B�܂��A�f�o�C�X�ɑ΂��鑀��R�}���h�ɑ΂��ẮA�O���T�[�o����A�N�Z�X���ɁA�܂��́A���s�\�Ƃ���B
�y�\3-3�z
API�̃T�[�r�X�@�\
�����`��
���͌`��
�o�^�f�o�C�X�̃v���p�e�B���̎擾
JSON

�o�^�f�o�C�X�̃m�[�h���X�g�iIP�A�h���X�j�̎擾
JSON

�������Ă���f�o�C�X�̃m�[�h���X�g�iIP�A�h���X�j�̎擾
JSON

�������Ă���S�f�o�C�X�̌��ݒl�̎擾
JSON

�������Ă���f�o�C�X�̂�������f�o�C�X�̌��ݒl�̎擾
JSON

����f�o�C�X�ւ̏������݋@�\
JSON
JSON
�Ǘ��Ώۃf�o�C�X��Id�̒ǉ��y�сA�폜�@�\
JSON
JSON
�e�f�o�C�X�̎擾�I�u�W�F�N�g�ƃv���p�e�B�̐ݒ�
JSON
JSON

3.1.7 COV�Ǘ����W���[�������COV�ʒm����M�^���M�y�уf�[�^�̓������@�\

* COV�Ǘ����W���[����WebSocket�N���C�A���g�Ƃ��Đ����ʒm����M�\�Ȃ悤��WebSocket�T�[�o�[���\��������B
* �ʒm����M�����^�C�~���O�ŊY���I�u�W�F�N�g�̌��ݒl��ʒm���e�ɏ]������������悤�ɍ\������B

3.2 BACnet-WOT�ϊ��@�\

�@BACnet�Ǘ��@�\�ƓK���ʐM���s���A�����_�ł̃f�o�C�X�����擾����B�擾�����f�o�C�X�������ƂɁA�f�o�C�X�^�C�v�ɉ������V���O�𐶐�����B�Ǘ��T�[�o�̏��́ABACnet-WOT�ϊ��T�[�o�N�����ɐݒ�t�@�C���Ƃ��Ē�`����B
�@�ݒ�t�@�C���Ƃ��ẮA�ȉ��̏����܂ށB

�y�\3-4�z�@ver.0.4.9
����(constants)
����
�����l
url
BACnet�f�o�C�X�Ǘ��T�[�o�̃A�N�Z�X�|�C���g
Default: localhost:5000
db_url
mysql�����T�[�o�[�̃A�N�Z�X�|�C���g
Default: localhost:3000
interval
���ݒl�|�[�����O����
Default: 30�b
update_interval
WOT�̃v���p�e�B�l�̊Ď�����
Default: 3�b
diff_interval
WOT�̃v���p�e�B�l�̍�������
Default: 60�b
proto
Discovery�v���g�R��
Default: mdns
test
DB�̗��p�L��
Default: false�i���p�j
devIds
�f�o�C�X���̋���prefix
Default: []


����(event_objects)
����
��̗�
device_id
�f�o�C�X��Id 
500�P
object
�ȉ��̃I�u�W�F�N�g�̔z��Œ�`�L�[�F�I�u�W�F�N�gId
�l�F�ȉ��̃I�u�W�F�N�g���`
�L�[�F�C�x���g���A�����A�C�x���g�Ώۂ̃I�u�W�F�N�g�̌^�Ƃ��̒l
[{"binaryValue:1": {
  "event_name": "bv",
  "description": "The state of the sensor.",
  "type": "boolean"}}]

��̗�Fbacnet_test_event.json
{
  "constants":  {
      "url": "http://192.168.100.15:5000",
      "db_url": "http://192.168.100.15:3000",
      "port": 8000,
      "interval": 30,
      "polling": 60,
      "update_interval": 3,
      "diff_interval": 60,
      "proto": "mdns",
      "test": false,
      "devIds": ["aaa"]
  },
  "event_objects": [
    {
      "device_id": 599,
      "object": [{"multiStateValue:1": {
        "event_name": "update_interval","description": "The event for the updated interval time."
      }}]
    },
    {
      "device_id": 5001,
      "object": [{"binaryValue:1": {
        "event_name": "bv","description": "The state of the sensor.","type": "boolean"
      }}]
    },
......................................................................................................
    {
      "device_id": 5020,
      "object": [{"binaryValue:1": {
        "event_name": "bv","description": "The state of the sensor.","type": "boolean"
      }}]
    },
    {
      "device_id": 5021,
      "object": [
        {
          "binaryValue:0": {
          "event_name": "bi_0","description": "The state of the sensor.","type": "string"
          }
        },
        {
          "binaryValue:1": {
          "event_name": "bi_1","description": "The state of the sensor.","type": "string"
          }
        },
        {
          "binaryValue:2": {
          "event_name": "bi_2","description": "The state of the sensor.","type": "string"
          }
        },
             .........................................................................................................
        {
          "binaryValue:9": {
          "event_name": "bi_9","description": "The state of the sensor.","type": "string"
          }
        }
      ]
    }
  ]
}
ver.0.5.7�ȍ~�iEvent��`�̏����ύX�j
��̗�Fbacnet_light_event.json

---
3.2.1 �o�^�f�o�C�X�̏��̎擾�@�\
* BACnet�f�o�C�X�Ǘ��T�[�o�iBACnet�Ǘ��@�\�j�������I�ɓo�^�f�o�C�X�̏����擾����B
* BACnet�f�o�C�X�Ǘ��T�[�o�̃A�N�Z�X�|�C���g�y�сA�T�������͐ݒ�t�@�C������擾����B

3.2.2 �f�o�C�X�̐U�镑�����`����V���O��`�@�\
* �擾�����f�o�C�X�̃v���p�e�B�������Ƀf�o�C�X�̐U�镑�����`����B��̓I�ɂ́A�ȉ��̂悤�Ȓ�`���ڂ�����B�i�Z�N�V����6���Q�Ɓj
* ����id�Ɋւ��ẮA�O����DB�T�[�o�ɗ\�ߓo�^����uuid�����Ƃɐݒ肷�邱�ƂƂ��āA���O�ɓo�^���Ȃ��ꍇ�Ɋւ��Ă̂ݎ����������邱�ƂƂ���B���}�Q�Ɓj����ɂ��r��OS�̓��̃N���C�A���g�Ō��肵��Id�Ƃ̐�������S�ۂ��邱�Ƃ��\�ƂȂ�B



                        �y�}3�z

�y�\3-5�z �V���O���`�i��������CO2�Z���T�[���ɋL�ځj
���
�^
Thing Description�ւ̃}�b�s���O
�l�i��j
id
string
urn:bacnet:uuid�Ȃǈ�ӂ̒l���`
DB�T�[�o����Bacnet ID�ɑΉ�����uuid���擾���Đݒ�A������`�̏ꍇ�͎�������
"id": "urn:bacnet:c79df5d2-ec64-4367-9d5c-88572625440a",
title
string
BACnet�f�o�C�X�̃I�u�W�F�N�g��������
BACnet��device�I�u�W�F�N�g�̖��O��ݒ肷��B
"title": ""rapi3_device",
@type
Array
[string]
BACnet�f�o�C�X�̎�ނ��킩��悤�ɒ�`
[BACnet-Device]
Properties
JSON
�E�v���p�e�B���́ABACnet�f�o�C�X�̊e�I�u�W�F�N�g�ɑ΂��Ē�`���Ă���I�u�W�F�N�g���������Ă�B
�Etitle�́A��L�v���p�e�B���̐���
�Etype�́A��L�v���p�e�B�l�̌^
�E@type�́A��L�v���p�e�B�̃^�C�v

�E�I�u�W�F�N�g��minPresValue���́AmaxPreValue����`����Ă����TD��minimum�y��maximum�Ɋ����Ă�B
�E�I�u�W�F�N�g���AAnalogInput����BinaryInput�Ȃ��readOnly�L�[��ǉ�����true���Z�b�g����B
�Eunits����`����Ă���΁A"unit"�L�[�Ɋ����Ă�B
�T�v�̃L�[��BACnet���ɂȂ����TD�ɂ͐������Ȃ��B

�ȉ����Q�ƁB
bacpypes/py34/bacpypes/basetypes.py at master ? JoelBender/bacpypes ? GitHub


{
  "CO2_av": {
  "title": "co2 concentration",
  "type": "integer",
  "@type": "LevelProperty",
  "minimum": 0,
  "maximum": 9999.,
  "readOnly": true,
  "unit": "partsPerMillion",
  "description": ".......",
},
{
  "temp_ai": {
  "title": "temp_ai",
  "type": "number",
  "@type": "LevelProperty",
  "minimum": 0.0,
  "maximum": 55.0,
  "readOnly": true
  "unit": "degreesCelsius",
  "description": ".......",
},

Actions
JSON
POST�n�̑��삪����Β�`����

Events
JSON
��ԁ^�x��Ď��p�ɒǉ�


�y�\3-6�z�ϊ��ΏۃI�u�W�F�N�g�^�i�X��ނɌ���j
�I�u�W�F�N�g�^
�Ώ�
�ǂݏ���
TD�ɒǉ�����L�[
analogInput
��Ԓl
read
readOnly: true
analogValue
��ԁ^�ݒ�l
read/write
readOnly: false
writeOnly: false
analogOutput
�ݒ�l
write
writeOnly: true
binaryInput
��Ԓl
read
readOnly: true
binaryValue
��ԁ^�ݒ�l
read/write
readOnly: false
writeOnly: false
binaryOutput
�ݒ�l
write
writeOnly: true
multiStateInput
��Ԓl
read
readOnly: true
�񋓌^�L�[enum��ǉ�����stateText�����蓖�Ă�B
multiStateValue
��ԁ^�ݒ�l
read/write
readOnly: false
writeOnly: false
�񋓌^�L�[enum��ǉ�����stateText�����蓖�Ă�B
multiStateOutput
�ݒ�l
write
writeOnly: true
�񋓌^�L�[enum��ǉ�����steteText�����蓖�Ă�B

---

3.2.3 �����f�[�^�]���@�\�y�񓯊��ʐM����������Event�@�\
�@�Ď��^�N���C�A���g��z�肵�āA�擾�f�[�^���ȉ��̂Q�ɕ��ނ��ăf�[�^�^�ɉ������]���@�\����������B
?@ ���n��v���f�[�^�̊Ď�
�@���n��v���f�[�^�Ƃ��ẮA��{�I�ɑΏۂƂȂ�f�o�C�X�̃v���p�e�B�[����莞�Ԃ��Ƃɂ��ׂĎ��W����B���������Ė{�f�[�^�ɑ΂��ẮA�r��OS���������I�Ƀ|�[�����O���āA���邢�͔C�ӂ̃^�C�~���O�őS�f�[�^�̓Ǐo�����s���B
�@�������A�ω��̂Ȃ��f�[�^�𖈉�ǂ݂������Ƃ̓V�X�e���ւ̕��ׂ��傫�����߁A�ω��̂������f�[�^������ʒm���Čʂɓǂݏo���@�\���񋟂���B
?A ��ԋy�ьx��Ȃǂ̔񓯊��f�[�^�̊Ď�
�@WoT�����ẮA�񓯊��ɔ�������C�x���g�̒ʒm�Ƃ��āAHTTP long-polling��WebSocket��2�̕��@��������Ă���(https://wot-jp-cg.netlify.app/docs/basicsequence/)�B�{�d�l���Ɋ�Â�����̎����ł́A�������S�̏��Ȃ�long polling��p�����������s���Ƃ���B

�ELong-polling�̎�����
https://www.turtle-techies.com/long-pollng-nodejs/
���Q�l�ɂ��āA�ȉ��̃C�x���g�G�~�b�^�̎������s���B



Event.js
�y�R�[�h1�z

���}�ɁA�N���C�A���g����̃��N�G�X�g�ɂ���ăT�[�o�[���C�x���g��o�^�y�ю��s���闬��������B�T�[�o�[�́A�N���C�A���g���烊�N�G�X�g���󂯂�ƃC�x���g��o�^����B�����ĉ�������f�[�^�̏������ł���܂Ō����ێ�����B�f�[�^�������ł����i�K�ŃN���C�A���g�Ƀf�[�^���������闬��ƂȂ�B



��̓I�ȁA�T�[�o�[�̃C�x���g���������̃R�[�h�̈ꕔ���Q�l�܂łɈȉ��Ɏ����B
Server.js
�y�R�[�h2�z
............................................................................................................................
app.get('/', function (req, res) {
   const id = Date.now().toString(); // milliseconds of now will be fine for our case
   var timer = null;
   const handler = function(event) {
      clearTimeout(timer);
      console.log('event', event);
      res.status(201);
      res.end( JSON.stringify(event));
   };

   eventEmitter.register(id, handler);
   timer = setTimeout(function(){ 
      console.log('timeout');
      const wasUnregistered = eventEmitter.unregister(id);
      console.log("wasUnregistered", wasUnregistered);
      if (wasUnregistered){
         res.status(200);
         res.end();
      }
   }, 5000);
});
......................................�@�ȗ��@...................................................................................


3.2.4 �e�V���O��������WOT�T�[�o���J�n����@�\
* Mozilla��Web things�̃t���[�����[�N�ɏ]��WOT�T�[�o���N������B
* �eWOT�T�[�o�́ABACnet�f�o�C�X�Ǘ��T�[�o��API�T�[�r�X����ăf�o�C�X�̍ŐV�����|�[�����O���ăV���O�Ƃ̓��������s���B
* �N���C�A���g�A�v���iADT���܂ށj����f�o�C�X�ւ̑���𔺂��ꍇ�́AWOT�T�[�o����ABACnet�f�o�C�X�Ǘ��T�[�o����Ċe�f�o�C�X�ɃR�}���h�𑗐M����B

�y�}4�z


---

3.2.5 �o�^�f�o�C�X���̊Ď��@�\
�@BACnet�f�o�C�X�Ǘ��T�[�o����̓o�^�f�o�C�X�i�m�[�h�j�̏���ێ����Ă����B����A�Ď����ɓo�^�m�[�h�ɕύX���Ȃ���΁A��莞�Ԍ�ēx�o�^�m�[�h�𒲂ׂ�B�o�^�m�[�h�ɕύX�i�ǉ��E�폜�j�����m������A���݂̃T�[�o���~������B�ēx�V�����f�o�C�X�����Ǘ��T�[�o���炩��擾���āA�V���O�̍\�����Ē�`����B���̌�A�ēxWOT�̃T�[�r�X���J�n����B
�@
3.2.6 COV�Ǘ����W���[�������COV�ʒm����M�y�ё��M����@�\

 �@BACnet�Ǘ��T�[�o�[�̍\���Ɠ��l�ɁACOV�Ǘ����W���[����WebSocket�N���C�A���g�Ƃ��Đ����ʒm����M�\�Ȃ悤��WebSocket�T�[�o�[���\������B

COV�ʒm�ɂ��f�[�^�������y�у����O�|�[�����O�����@�\

�ʒm����M�����^�C�~���O�ŊY���v���p�e�B�̌��ݒl��ʒm���e�ɏ]������������悤�ɍ\������B�����ɁA�ʒm���e�ɏ]���C�x���g�G�~�b�^�[���g���K�[���ă����O�|�[�����O�ւ̉������쐬���ăN���C�A���g�ɕԂ��\���Ƃ���B

���}�ɋ�̓I�ȗ�Ƃ���COV�ʒm�ƃ����O�|�[�����O�ւ̉����܂ł̗���������B



---

3.3 ID�ϊ��@�\
�@�}�R��ID�ϊ����W���[���ɑΉ�����@�\�ł���B�V���O�̐������ɂ���wot_id��BACnet�f�o�C�XId�Ƃ̕R�Â�����ɂ����Ȃ��@�\��S���B�����A�f�o�C�XId�ɂ͈�̃V���O�̑Ή���z�肵�Ă������A�����ւ̓K�p���i����C�ɂ�����BACnet�V�X�e���j�ɁA����BACnet�f�o�C�X���̂ɘ_���I�ȃf�o�C�X�̍\�����ێ������邱�Ƃ������������߂Ɉȉ��̂悤�Ɋg�����s���B��{�I�Ƀf�o�C�XId��wot_id�͂P�΂P�Ή����邪�A�f�o�C�X���Q�ȏ�̃V���O�ō\������Ă��邱�Ƃ��������߂ɃV�[�P���XId��V���ɓ�������B�ȉ��ɋ�̓I�ȃf�[�^�x�[�X�̐݌v����Q�l�܂łɒ񎦂��Ă����B
3.3.1 �f�[�^�[�x�[�X�̍\��

�}�X�^�[���R�[�h�́A�f�o�C�XId��wot_id�y�ј_���I�ɉ��Ԗڂ̃V���O�ɂȂ�̂��𖾎����邽�߂�seq_id�ō\�������B�X�ɁA�t���I�ɂ��̃f�o�C�X���_���\�������ꍇ�ɂ́A�I�u�W�F�N�g�Ǘ����R�[�h���쐬���Ĉȉ��̂悤�ɁA���̃V���Owot_id���\������I�u�W�F�N�g���\���������쐬����B
(a) �}�X�^�[���R�[�h
�y�\3-7�z
id
bigint(20) NOT NULL AUTO_INCREMENT COMMENT 'id',
sub_system_id
TEXT
device_id
MEDIUMINT
seq_id
INT
wot_id
VARCHAR(255)
created_at
TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT '�쐬����',
updated_at
TIMESTAMP  NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '�X�V����',
(b) �I�u�W�F�N�g�Ǘ����R�[�h
�y�\3-8�z
id
bigint(20) NOT NULL AUTO_INCREMENT COMMENT 'id',

wot_id
VARCHAR(255)
object_id
VARCHAR(20)
alias
VARCHAR(80)
created_at
TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT '�쐬����',
updated_at
TIMESTAMP  NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT '�X�V����',
���݂ɁA�I�u�W�F�N�g�Ǘ����R�[�h��alias�J������݂��Ă��邪�I�u�W�F�N�g��wot�ϊ������ꍇ�ɁA�f�t�H���g�ł̓I�u�W�F�N�g����wot�̃v���p�e�B�Ƀ}�b�s���O����d�l��z�肵�Ă��邪�A�W�Lalias�J�������`���邱�Ƃɂ��C�ӂɃ��[�U�[���t�^���閼�O�ɒu�������邱�Ƃ��\�Ƃ���B

3.3.2 �f�[�^�[�x�[�X����@�\

�@�O�߂Œ�`�����f�[�^�x�[�X�𑀍���邽�߂̋@�\����������B
���\�ɋ�̓I�ȑ���ꗗ�������B���݂ɁAid_map2: �}�X�^�[���R�[�h�y��object_map2: �I�u�W�F�N�g�Ǘ����R�[�h�ɑΉ�����B�iid_map�y��object_map�́A�d�l�ύX�O�Ɏg�p���Ă����`���j

�y�\3-9�z
�T�[�r�X�|�C���g
���\�b�h
�N�G��
�{�f�B
����
/create_table
POST
tbl=id_map
�@
�V�K�e�[�u���̍쐬�B
��) id_map�y��object_map�́A���łƂ̐������ׂ̈Ɏc��


default: id_map2


/ceate_data
POST
�@
index_n��ǉ�
wot_id�̎��������B




index�J������ǉ��B
/insert
POST
tbl=object_map
index��ǉ�
index�J������ǉ��ɑΉ�


default: id_map2


/map_object
GET
device_id

wot_id��object_id�Ƃ̕R�Â�
�N�G��alias�ŁAobject_map2�̃��R�[�h���擾����


index
�@



alias
�@


POST
device_id
�@
alias=1�̏ꍇ�Aobject_map2�̃��R�[�h�Ƀf�[�^��o�^����B
alias_names: ������̔z��Œ�`����B


index
�@



alias
�@

/inquire
GET
tbl, wot_id,
�@
�@


device_id
�@

/register
GET
tbl=id_map2
�@
�@


object_map
�@

/table_remove
DELETE
tbl=id_map2
�@
�e�[�u�����폜


object_map
�@


��̓I�ȑ���菇�́A�ȉ��̂Ƃ���B
@host = db_url
1. �}�X�^�[�e�[�u���̍쐬
   POST {{host}}/create_table?tbl=id_map2
   Content-Type: application/json

2. �}�X�^�[�e�[�u���ɓo�^
�EdeviceId��5001����5020��V�K�o�^
POST {{host}}/create_data
Content-Type: application/json

{
   "tbl": "id_map2",
    "sub_system_id": "bacnet",
    "device_ids": ["5001-5020"],
    "index_n": 1
}

3. �I�u�W�F�N�g�e�[�u���̍쐬�i�_���\��������ꍇ�j
POST {{host}}/create_table?tbl=object_map2
Content-Type: application/json

4. �I�u�W�F�N�g�e�[�u���ɓo�^�i�Ɩ��f�o�C�X�̏ꍇ�j
   POST {{host}}/map_object_all?alias
   Content-Type: application/json

< ./object.json

object.json�i��̗�j:

3.4 COV�ʒm�@�\
3.4.1 �f�o�C�X���擾�@�\
�E����l�b�g���[�N�ɐڑ�����Ă���BACnet�f�o�C�X�̏����擾����@�\ 

3.4.2 ���M�E��M�@�\
�ECOV�o�^�N���C�A���g�����M�́AWebSocket��p����ƂƂ��ɁA�e�T�[�o�[�ւ�COV�ʒm����������S�ۂ��邽�߂�WebSocket��p���č\�����邱�ƂƂ���B 

3.4.3 �o�^���擾�@�\
�E�����_�ŊeBACnet�f�o�C�X�ɐݒ肳��Ă���COV�o�^�����擾����@�\

3.4.4 �o�^/�����@�\
�ECOV�ɂ��ʒm�ݒ��ΏۂƂ���BACnet�f�o�C�X�̃I�u�W�F�N�g�ɑ΂��čs���ƂƂ��ɁA�s�v�ƂȂ����ݒ���폜���邽�߂̋@�\

�E�R�}���h��M�d�l�i������j�F
�y�\3-10�z
��{�`��


�L�[��
�^
����
header
�I�u�W�F�N�g
?@���Q��
body
�I�u�W�F�N�g�A
�I�u�W�F�N�g�̔z��
?A�A?B���Q��



?@header�L�[
�o�^�^����

�L�[��
�^
����
version
����
�o�[�W�����w��
messageType
������
commandRequest'�Œ�l
messagePurpose
������
SubscribeCOV, UnSubscribeCOV,
COVList, WhoIS



?Abody�L�[
�o�^

�L�[��
�^
����
addr
������
�Ώۃf�o�C�X��IP
objectIds
������
�I�u�W�F�N�gId
lifetime
����
�ʏ�0��ݒ�



?Bbody�L�[
����

�L�[��
�^
����
addr
������
�Ώۃf�o�C�X��IP
group
�I�u�W�F�N�g�̔z��
?C���Q��
lifetime
����
�ʏ�1��ݒ�



?Cgroup�L�[�i�ȉ��̃I�u�W�F�N�g�̔z��j

�L�[��
�^
����
proc_id
������
�Ώۃf�o�C�X��IP
objectId
������
�I�u�W�F�N�gId
�o�^���f�[�^��F
�������f�[�^��F




















�o�^���f�[�^��i�����w��j�F
3.4.5 COV�ʒm�@�\
�ECOV�ݒ肵��BACnet�f�o�C�X����COV�ʒm��������BACnet�Ǘ��T�[�o�[�y��WOT�ϊ��T�[�o�[�ɓ]������@�\

3.4.6 ���̑�COV�Ǘ��T�[�o�[�̋@�\
�E��L�@�\��COV�Ǘ��N���C�A���g���痘�p���邽�߂Ɉȉ��̋@�\�������B

�ȉ��A������������B
�y�\3-11�z
�e�R�}���h�i�g�p�@�j
����
�^
�K�{
���l
����
upload <filename.json>
<filename.json>
������
��
�o�^/�����p�t�@�C����
�o�^/�����p�t�@�C����cov�Ǘ����W���[���ɑ��M����B
covlist <min/*> [max]  
<min/*>
����
��
�f�o�C�XId�ŏ��l
*�́A���C���h�J�[�h
min�`max�܂ł̃f�o�C�XId��cov�o�^�󋵂��擾����B

[max] 
����

�f�o�C�XId�ő�l

dblist
�@


�@
���ݓo�^����Ă���f�o�C�XId�ƃA�h���X�̏����擾����B
whois <min/*> [max] [broadcast]
<min/*>
����
��
�f�o�C�XId�ŏ��l
WhoIs�ɂ��min�`max�܂ł̃f�o�C�XId�̏��̎擾���s���B


Broadcast�i��j: 192.168.100.25:47809

[max]
����

�f�o�C�XId�ő�l


[broadcast]
������

�u���[�h�L���X�g

add_db <addr> <device_id>
<addr>
������
��
�f�o�C�X��IP�A�h���X
�@

<device_id>
����
��
�f�o�C�XId

remove <device_id>
<device_id>
����
��
�f�o�C�XId
�@




---


3.5 Azure Digital Twins�A�g�@�\
3.5.1 HTTP�v���g�R���ɂ�������
 Azure Digital Twins�i�ȉ�ADT�ƕ\���j���̌��݂̎d�l�́A�O���N���C�A���g����̃f�[�^�v�b�V���ɂ��e�c�C���̃v���p�e�B���X�V���邱�ƂɋK�肳��Ă���B����A�����_�ł�WoT�ϊ��T�[�o�[�́A�v���^�Ƃ��Ď������Ă��邽�߂Ƀv�b�V���^�ɕϊ�����@�\���K�v�ƂȂ�B�X�ɊO���N���C�A���g���琧�䂷��@�\��L����B
�]���āA�{�@�\�͈ȉ��́A�Q�̋@�\�ō\�������B�Ȃ��A3.3.2�߂�mqtt��p�����ʖ@���Q�l�܂łɋL�ڂ��Ă����B

(1) �v�b�V���^�̑��M�N���C�A���g�@�\
�@BACnet-WOT�ϊ��@�\�������I�ɊeWOT�̃v���p�e�B�l���擾����B�擾���ꂽWOT�̃f�[�^�́AADT���ŋK�肳�ꂽ�t�H�[�}�b�g�ɕϊ������B���̌�A�Ή�����f�W�^���c�C����PATCH���\�b�h�ɂ��f�[�^�̍X�V���s���B

(2) �A�g�@�\�𐧌䂷��T�[�o�[�@�\
 �O���N���C�A���g�iADT���܂ށj����̃��N�G�X�g�ɉ����āA�A�g�@�\����������T�[�o�[�@�\�B�擾���ꂽWOT�̃f�[�^���f�W�^���c�C���ւ̑��M�J�n�A�܂��͒�~���邽�߂̃��N�G�X�g�҂��Ƃ��̎��s�y�сA�f�[�^�X�V�Ԋu�̕ύX���N�G�X�g��҂��Ď��s����@�\�B
��̓I�d�l�́A�ȉ��̕\�R�|�V�Ƃ���B

�y�\3-12�z
�T�[�r�X�|�C���g
���\�b�h
���N�G�X�g
����
/wotpost/config
GET
�Ȃ�
�ݒ���̕\��
/wotpost/command
PUT
{"start": true}
Publish�J�n


{"stopt": true}
Publish��~


{"set_interval": 120000}
Publish�̎��ԊԊu�̐ݒ�



�y�}5�z ADT�A�g�@�\��ADT�Ƃ̊֌W�}

3.5.2 MQTT�v���g�R���ɂ�������
 ADT���̌��݂̎d�l���C�����邱�ƂɂȂ邪�AADT�����烍�[�J���iBACnet-GW�j���ւ̃R�}���h���M�����[�J�����̃O���[�o��IP�����J���邱�ƂȂ��������邽�߂̕���Ƃ���MQTT�ɂ��PUB/SUB�ɂ��f�[�^�ʐM�����̌������s���B

(1) PUB�T�[�o�[�@�\�i�N���C�A���g�@�\�܂ށj�iBACnet-GW�j
�@MQTT�T�[�o�[�́A�ʓr�z�u����Broker�Ƃ̐ڑ���A�R�}���h�҂���Ԃɓ���BBroker����ăN���C�A���g�i�r��OS�j����R�}���h���擾��A�R�}���h�ɉ�����������s���B�Ⴆ�΁A�X�V�J�n�̃R�}���h��MQTT�T�[�o�[����M����ƁA���̃N���C�A���g�@�\�́ABACnet-WOT�ϊ��@�\�������I�ɊeWOT�̃v���p�e�B�l�̎擾���J�n����B�擾���ꂽWOT�̃f�[�^�́AADT���ŋK�肳�ꂽ�t�H�[�}�b�g�ɕϊ������B���̌�A�Ή�����f�W�^���c�C����Broker����ăf�[�^��PUBLISH����ADT�̃f�[�^�X�V���s���B

(2) MQTT�N���C�A���g�@�\�i�Ď��N���C�A���g�F�r��OS�܂ށj
 BACnet-GW���ɔz�u���ꂽMQTT�T�[�o�[�@�\�ɑ΂��ĊO���N���C�A���g�i�r��OS���܂ށj�Ɏ������ꂽMQTT�N���C�A���g����X�V�J�n�y�сA�X�V��~�Ȃǂ̃R�}���h��Broker�����PUBLISH���s���@�\�B


       �y�}6�z MQTT�v���g�R���𗘗p����ADT�A�g�@�\�̍\����
�Q�l�܂łɃg�s�b�N�X�̐݌v�d�l���\3-8�Ɏ����B




�y�\3-13�z


3.5.3 COV�ʒm�@�\��z�肵��������

�y�}�V�z�@�S�̂̃V�X�e���\���}



��L�A3.5.1 HTTP�v���g�R���ɂ�����������Ɏd�l�ύX���s���B

�y�}8�z �S�̂̃t���[�}

</div>

#### 4 �J����

4.1 BACnet�Ǘ��@�\
�EBACnet�X�^�b�N
BACnet�f�o�C�X�Ƃ̖��ȒʐM�y�ѐ��䂪�K�v�Ȃ��߈ȉ��̃t���[�����[�N��p���Ď������s���B
�g�p����X�^�b�N�́A�ȉ��̒ʂ�B
�y�\4-1�z
���O
URL
���l
�]��
BACpypes
https://github.com/JoelBender/bacpypes.git
Python�Ŏ�������Ă���
��r�I�T���v�����[�����Ă���


�EAPI�T�[�o�@�\
�V���v���y�ьy�ʂȍ��ł���Flask���̗p����B
�E���؊�
�@�{�d�l���Ɋ�Â�BACnet-GW�̓��쌟�؂������Ȃ����Ƃ��āA�}�S�̂悤�Ȋ��ŕ]�����s���Ă���B�����ł́A���l�b�g���[�N��1���BACnet�f�o�C�X�iCO2�Z���T�j�y�сAWindows11�ɍ\�z����Docker���y��raspi4B���Docker���ɍ��vN���BACnet�f�o�C�X�iCO2�Z���T�V�~�����[�^�j��z�u����B�e�l�b�g���[�N�Ԃ́Aip2ip2���[�^��z�u���āAWho-Is�̃p�P�b�g���a�ʂ���悤�ɐݒ肷��B�@����Ώۂ�BACnet�f�o�C�X�́A�Z���T�[�n��z�肷�邱�ƂƂ���B

�y�}9�z ���쌟�؊�

4.2 BACnet-WOT�ϊ��@�\

�@Web Things���L�q���邽�߂̃t���[�����[�N�Ƃ��ẮA�����_�ŋƊE�W���Ǝv����Mozilla�̒񋟂��郉�C�u�������g�p����BBACnet�Ǘ��@�\��python�x�[�X�ł̎�����z�肵�Ă���̂ŁA�{���Ȃ��python�x�[�X�̃t���[�����[�N���]�܂������A����܂ł̎����R�[�h�̊��p��z�肵��node�x�[�X�̃t���[�����[�N���̗p����B
�y�\4-2�z web things�t���[�����[�N
���O
URL
�g�p���ꓙ
�]��
webthing-node
https://github.com/WebThingsIO/webthing-node
Node
�ߋ��̌o�܂��̗p
webthing-python
https://github.com/WebThingsIO/webthing-python
Python

webthing-java
https://github.com/WebThingsIO/webthing-java
Java

eclipse-thingweb/
node-wot
https://github.com/eclipse-thingweb/node-wot
Node



---

4.3 ���s��

�E�e�T�[�o�̎��s��
�@�{�d�l���Œ�`����BACnet-GW�iBACnet�Ǘ��T�[�o�@�\�y��BACnet-WOT�ϊ��T�[�o�@�\�j�́A�r�����[�J�����ɒu���ꂽGW�@���Ɏ�������^�p����邱�Ƃ�z�肷��B����GW�@��́A���^PC/�Y�ƗpPC��T�[�o�ȂǔC�ӂ̃v���b�g�t�H�[���Ƃ���B
�@��������ɂ����Ă�Windows11 GMK NucBox G1(Intel N95)��ɂāABACnet�Ǘ��T�[�o�y�сABACnet-WOT�ϊ��T�[�o�̎��s���������ĕ]�����s���Ă���B�A���ANative��Windows���Ŏ��s���邩�A�ێ琫���l�����āAWindows��ł�docker�R���e�i�Ƃ��ăf�v���C����Ȃǂ̑I�������z�肵�Ă���B

�y�}10�z ���s��

4.4�Q�l

4.4.1 BACnet�Ή�CO�Q�Z���T�[�̎���
 

4.4.2 BACnet�̊e�d�l��`
�y�\4-3�z �I�u�W�F�N�g�̎d�l
�I�u�W�F�N�g
����
Device
�f�o�C�X��
Analog Input:0
CO2�̏��
Analog Input:1
���x�̏��
Analog Input:2
���x�̏��
Analog Input:3
�o�b�e���[�̏��
Multi-State Value:1
�v�����ԊԊu�̐ݒ�

 �y�\4-4�z �T�|�[�g����T�[�r�X
�T�[�r�X
����
����
Who-is/ I-am
Discovery�T�[�r�X
��
Read Property
�I�u�W�F�N�g�̃v���p�e�B�̎擾
��
Write Property
�I�u�W�F�N�g�̃v���p�e�B�̍X�V
��



4.4.3 �t�@���R�C���G�~�����[�^�̎����i�]���p�j

 �y�\4-5�z�t�@���R�C���̎d�l
�ԍ�
�@�v���p�e�B��
�@Object�^
�@����d�l
1
�@ActVlvOpnRt
  (�o���u�J�x�j
�@analogInput
�E�������ݒ���Ⴂ�Ƃ��̂݊J�x���i��
�E��~���́A0%
IF (RmTemp��RmTempSpt)
       50-90%�ŗh�炬�i�����j
THEN
     100% (�S�J)
2
RoomTemp
�i�����j
�@analogInput
 �ݒ艷�x�}3.0�ŗh�炬�i�����j
  ��~���A�ŏI�l���ێ�
3
�@TempSetpt
�@analogValue

4
�@ActAlarm
�@binaryInput
�E�ݒ艷�x��35.0�ȏ��ݒ肵���Ƃ��A���[������
5
�@OnOffSt
�@binaryInput
�ECmd�̒l�𔽉f�i��莞�Ԃ��Ƃ�Cmd�̌��ݒl�𔽉f�j
6
�@OpModeSt
�@binaryInput
�EOpModeCmd�̒l�𔽉f
�i��莞�Ԃ��Ƃ�Cmd�̌��ݒl�𔽉f�j
7
�@Cmd
�@binaryOutput

8
�@OpModeCmd
�@binaryOutput




4.4.4 WOT���Ɍ�����BACnet�̎d�l�̌���


 �y�\4-6�z�@�I�u�W�F�N�g�v���p�e�B�̒�`

�I�u�W�F�N�g
�v���p�e�B
�^
�l�i��j
device
objectName
string
CO2_av

objectIdentifier
int
600

address
string
192.168.1.142/22:47808

maxApduLengthAccepted
int
1024

segmentationSupported
string
segmentedBoth

foreignBBMD
string
128.253.109.254

foreignTTL
int
30
Analog Input
objectName
string
CO2_av ...

objectIdentifier
tupple
("analogInput", i) i=0,3

presentValue
Real
200

statusFlags
[Integer]
[0,0,0,0]

covIncrement
Real, Integer
1.0

minPresValue
Real, Integer
0

maxPresValue
Real, Integer
1000

units
EngineeringUnits
partsPerMillion
Multi-State
Value
objectName
string
update_mv

objectIdentifier
tupple
("multistateValue", 1)

presentValue
Unsigned
15

statusFlags
[Integer,]
[0,0,0,0]

numberOfState
Integer
11

stateText
[string]
['5s','10s','15s','30s','1m','2m','3m','5m','10m','15m','30m']

���d�l�Ɋ�Â��p�����[�^�ݒ�
TR-76Ui�d�l
���荀��
����͈�
���x
�P��
CO2
0�`9999
�}50
ppm
���x
0�`55
�}0.5
��
���x
10�`95
�}5
%RH

BACnet �v���p�e�B
minPresValue
maxPresValue
units
0
9999
partsPerMillion
0
55
degreesCelsius
10
95
percentRelativeHumidity



[���R1]�ǉ��E�C������
?@2.3 COV�ʒm�@�\
?A3.1.6 COV�Ǘ��`
?B3.2.6 COV�Ǘ��`
?C3.4 COV�ʒm�@�\
?D 3.5.3 COV�ʒm�@�\��z�肵��������
