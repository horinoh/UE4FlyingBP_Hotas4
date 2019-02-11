# UE4FlyingBP_hotas4

## �K�p�̎d�� (How to apply)
- hotas4 ���Ȃ� (Connect hotas4)
- New Project - Blueprint - Flying �̃e���v���[�g��I�����ăv���W�F�N�g����� (New Project - Blueprint - Select Flying template and create project)
- Config/DefaultInput.ini ���㏑������ (Overwrite Config/DefaultInput.ini)
- Edit - Plugins - Input Devices - Windows RawInput ��L���ɂ��� (Edit - Plugins - Input Devices - Enable Windows RawInput)

## ��������� (What I have done)
- DefaultInput.ini
    - Raw Input �̐ݒ��ǉ����� (Added Raw Input settings)
    - MoveUp, MoveRight, Thrust �� GenericUSBController_Axis<N> ��ǉ� (Added GenericUSBController_Axis<N> to MoveUp, MoveRight, Thrust)
~~~
[/Script/RawInput.RawInputSettings]
+DeviceConfigurations=(VendorID="0x044F",ProductID="0xB67C",AxisProperties=((Key=GenericUSBController_Axis1,bInverted=True,Offset=0.500000),(Key=GenericUSBController_Axis2,Offset=-0.500000),(Key=GenericUSBController_Axis3,Offset=-0.500000),(bEnabled=False,Key=GenericUSBController_Axis4),(bEnabled=False,Key=GenericUSBController_Axis5),(bEnabled=False,Key=GenericUSBController_Axis6),(Key=GenericUSBController_Axis7,Offset=-0.500000),(Key=GenericUSBController_Axis8,bInverted=True,Offset=0.500000)),ButtonProperties=((Key=GenericUSBController_Button1),(Key=GenericUSBController_Button2),(Key=GenericUSBController_Button3),(Key=GenericUSBController_Button4),(Key=GenericUSBController_Button5),(Key=GenericUSBController_Button6),(Key=GenericUSBController_Button7),(Key=GenericUSBController_Button8),(Key=GenericUSBController_Button9),(Key=GenericUSBController_Button10),(Key=GenericUSBController_Button11),(Key=GenericUSBController_Button12),(Key=GenericUSBController_Button13),(Key=GenericUSBController_Button14),(Key=GenericUSBController_Button15),(Key=GenericUSBController_Button16),(Key=GenericUSBController_Button17),(Key=GenericUSBController_Button18),(Key=GenericUSBController_Button19),(Key=GenericUSBController_Button20)))
~~~
~~~
[/Script/Engine.InputSettings]
...
+AxisMappings=(AxisName="MoveUp",Scale=2.000000,Key=GenericUSBController_Axis1)
+AxisMappings=(AxisName="MoveRight",Scale=2.000000,Key=GenericUSBController_Axis2)
+AxisMappings=(AxisName="Thrust",Scale=2.000000,Key=GenericUSBController_Axis8)
~~~
