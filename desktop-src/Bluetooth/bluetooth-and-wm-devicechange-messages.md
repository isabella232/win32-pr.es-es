---
title: Bluetooth y WM_DEVICECHANGE mensajes
description: Bluetooth incluye mensajes WM DEVICECHANGE específicos que permiten a los desarrolladores obtener mensajes cuando Bluetooth \_ dispositivos sufren cambios de estado.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172093"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>mensajes Bluetooth y WM \_ DEVICECHANGE

Bluetooth incluye mensajes [**ESPECÍFICOS DE WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) que permiten a los desarrolladores obtener mensajes cuando Bluetooth dispositivos sufren cambios de estado. En este tema se describe cómo recibir mensajes Bluetooth **WM \_ DEVICECHANGE** específicos y listas Bluetooth mensajes específicos.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Recepción Bluetooth mensajes WM \_ DEVICECHANGE específicos

Para recibir [**mensajes \_ DE WM DEVICECHANGE,**](/windows/desktop/DevIO/wm-devicechange) primero debe abrirse un identificador para la radio local. Para ello, use uno de estos métodos:

-   Use la función [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con los parámetros siguientes: (GUID BTHPORT DEVICE INTERFACE, ..., DIGCF PRESENT DIGCF DEVICEINTERFACE) y, a continuación, use las funciones \_ \_ \_ \_ \| \_ [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail,](https://msdn.microsoft.com/library/ms792901.aspx) [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)y [SetupDiDestroyDeviceInfoList.](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
-   Use las [**funciones BluetoothFindFirstRadio,**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio) [**BluetoothFindNextRadio y**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio) [**BluetoothFindRadioClose.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)

Cuando se Bluetooth identificador de radio, llame a la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) y regístrese para recibir notificaciones en el identificador mediante **DBT \_ DEVTYP \_ HANDLE** como devicetype. Cuando se registra, se envían los siguientes GUID y el miembro de datos [**\_ DEV BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_** es el búfer asociado.

## <a name="bluetooth-specific-messages"></a>Bluetooth específicos de la aplicación

En la tabla siguiente se Bluetooth [**mensajes WM \_ DEVICECHANGE específicos.**](/windows/desktop/DevIO/wm-devicechange)

| GUID                                   | BUFFER                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENTO \_ DE BLUETOOTH \_ HCI \_ GUID            | [**BTH \_ HCI \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Este mensaje se envía cuando un dispositivo Bluetooth se conecta o se desconecta en el nivel de ACL.                                                                                                                                                                                                                                                                    |
| EVENTO \_ L2CAP DE BLUETOOTH \_ \_ GUID          | [**BTH \_ L2CAP \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Este mensaje se envía cuando se ha establecido o finalizado un canal L2CAP entre la radio local y un Bluetooth remoto. En el caso de los canales L2CAP que son multiplexores, como RFCOMM, este mensaje solo se envía cuando se establece el canal subyacente, no cuando se establece o finaliza cada canal multiplexado, como un canal RFCOMM. |
| SOLICITUD DE \_ PIN DE BLUETOOTH \_ \_ GUID          | No aplicable.                                         | La aplicación debe omitir este mensaje. Si la aplicación debe recibir solicitudes de PIN, se debe usar la función [**BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)                                                                                                                                                   |
| RADIO \_ BLUETOOTH GUID EN \_ \_ \_ INTERVALO      | [**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Este mensaje se envía cuando cualquiera de los siguientes atributos de un dispositivo Bluetooth remoto ha cambiado: el dispositivo se ha detectado, la clase del dispositivo, el nombre, el estado conectado o el estado de recordar del dispositivo. Este mensaje también se envía cuando se establecen o borran estos atributos.                                                                                  |
| RADIO \_ BLUETOOTH GUID FUERA DEL \_ \_ \_ \_ INTERVALO | [**DIRECCIÓN \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Este mensaje se envía cuando no se ha encontrado un dispositivo detectado previamente después de la finalización de la última consulta. Este mensaje no se enviará para los dispositivos que se recuerden. La **estructura \_ BTH ADDRESS** es la dirección del dispositivo que no se encontró.                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**DIRECCIÓN \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**BTH \_ HCI \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**BTH \_ L2CAP \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**IDENTIFICADOR DE DIFUSIÓN \_ DE \_ DESARROLLO**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 