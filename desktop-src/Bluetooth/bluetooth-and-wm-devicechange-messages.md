---
title: Mensajes de WM_DEVICECHANGE y Bluetooth
description: Bluetooth incluye \_ mensajes DEVICECHANGE específicos de WM que permiten a los desarrolladores obtener mensajes cuando los dispositivos Bluetooth se someten a cambios de estado.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995342"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Mensajes de DEVICECHANGE de Bluetooth y WM \_

Bluetooth incluye mensajes [**\_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) específicos de WM que permiten a los desarrolladores obtener mensajes cuando los dispositivos Bluetooth se someten a cambios de estado. En este tema se describe cómo recibir mensajes de **WM \_ DEVICECHANGE** específicos de Bluetooth y se enumeran los mensajes específicos de Bluetooth.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Recepción de mensajes DEVICECHANGE de WM específicos de Bluetooth \_

Para recibir mensajes de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , primero se debe abrir un identificador para la radio local. Para ello, use uno de estos métodos:

-   Use la función [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con los siguientes parámetros: ( \_ \_ interfaz de dispositivo GUID BTHPORT \_ ,..., \_ DIGCF \| present DIGCF \_ DEVICEINTERFACE) y, a continuación, use las funciones [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)y [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .
-   Use las funciones [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)y [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

Cuando se abra el controlador de radio Bluetooth, llame a la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) y regístrese para recibir notificaciones en el identificador mediante **DBT \_ DEVTYP \_ Handle** como DeviceType. Cuando se registra, se envían los siguientes GUID y el miembro de datos [**\_ \_ Handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_** de dev es el búfer asociado.

## <a name="bluetooth-specific-messages"></a>Mensajes específicos de Bluetooth

En la tabla siguiente se enumeran los mensajes de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) específicos de Bluetooth.

| GUID                                   | BUFFER                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ evento HCI de Bluetooth de GUID \_            | [**BTH \_ \_ información de evento de HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Este mensaje se envía cuando un dispositivo Bluetooth remoto se conecta o se desconecta en el nivel de ACL.                                                                                                                                                                                                                                                                    |
| \_ \_ Evento L2CAP de Bluetooth de GUID \_          | [**BTH \_ \_ información de evento de L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Este mensaje se envía cuando se ha establecido o finalizado un canal L2CAP entre la radio local y un dispositivo Bluetooth remoto. En el caso de los canales L2CAP que son multiplexores, como RFCOMM, este mensaje solo se envía cuando se establece el canal subyacente, no cuando se establece o finaliza cada canal multiplexado, como un canal RFCOMM. |
| \_solicitud de \_ PIN de Bluetooth de GUID \_          | No es aplicable.                                         | La aplicación debe pasar por alto este mensaje. Si la aplicación debe recibir solicitudes de PIN, se debe usar la función [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                                                                                                                   |
| \_radio Bluetooth \_ de GUID \_ en el \_ intervalo      | [**\_radio BTH \_ en el \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Este mensaje se envía cuando cambia cualquiera de los siguientes atributos de un dispositivo Bluetooth remoto: se ha detectado el dispositivo, la clase de dispositivo, el nombre, el estado conectado o el estado recordado del dispositivo. También se envía este mensaje cuando se establecen o borran estos atributos.                                                                                  |
| \_radio Bluetooth \_ \_ de GUID fuera \_ del \_ intervalo | [**\_dirección Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Este mensaje se envía cuando no se ha encontrado un dispositivo detectado anteriormente después de la finalización de la última consulta. Este mensaje no se enviará para dispositivos recordados. La estructura de **\_ direcciones BTH** es la dirección del dispositivo que no se encontró.                                                                                                      |



 

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

[**\_dirección Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**BTH \_ \_ información de evento de HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**BTH \_ \_ información de evento de L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**\_radio BTH \_ en el \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**\_controlador de difusión de dev \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**DEVICECHANGE de WM \_**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 