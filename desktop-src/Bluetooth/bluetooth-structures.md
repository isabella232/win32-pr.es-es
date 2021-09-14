---
title: Bluetooth Estructuras
description: En esta sección se proporcionan definiciones de estructuras que se usan para administrar Bluetooth dispositivos y servicios.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, referencia, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df10989e41814f6f750bdcc719f01b14ccae315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261847"
---
# <a name="bluetooth-structures"></a>Bluetooth Estructuras

En esta sección se proporcionan definiciones de estructuras que se usan para administrar Bluetooth dispositivos y servicios.

Bluetooth también se admite mediante la interfaz de programación Windows Sockets. Para obtener más información sobre la programación Bluetooth mediante la interfaz Windows Sockets, vea Compatibilidad con sockets Windows [sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sección                                                                                       | Contenido                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**DIRECCIÓN \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contiene la dirección de un Bluetooth dispositivo.                                                                                      |
| [**AUTENTICACIÓN DE BLUETOOTH \_ \_ PARAMS DE \_ DEVOLUCIÓN DE LLAMADA**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contiene información de configuración específica sobre el dispositivo Bluetooth respuesta a una solicitud de autenticación.                  |
| [**RESPUESTA \_ DE AUTENTICACIÓN \_ DE BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contiene información que se pasa en respuesta a un evento \_ BTH REMOTE \_ AUTHENTICATE \_ REQUEST.                                           |
| [**PARES DE COD DE BLUETOOTH \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Proporciona especificación y recuperación de Bluetooth información de clase de dispositivo (COD).                                         |
| [**INFORMACIÓN \_ DEL DISPOSITIVO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Proporciona información sobre un Bluetooth dispositivo.                                                                                   |
| [**PARAMS \_ DE BÚSQUEDA \_ DE \_ DISPOSITIVOS BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Especifica los criterios de búsqueda para Bluetooth búsquedas de dispositivos.                                                                         |
| [**BLUETOOTH \_ FIND \_ RADIO \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Facilita la enumeración de radios Bluetooth instaladas.                                                                       |
| [**INFORMACIÓN \_ DEL SERVICIO LOCAL \_ \_ DE BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contiene información de servicio local para una Bluetooth radio.                                                                        |
| [**INFORMACIÓN DE \_ COMPARACIÓN \_ NUMÉRICA DE \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contiene el valor numérico utilizado para la autenticación a través de la comparación numérica.                                                       |
| [**INFORMACIÓN \_ DE DATOS DE BLUETOOTH \_ \_ OOB**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contiene los datos usados para autenticarse antes de establecer un emparejamiento de dispositivos fuera de banda.                                          |
| [**INFORMACIÓN \_ DE CLAVE DE PASO DE \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contiene la clave de paso usada para la autenticación a través de la clave de paso.                                                                        |
| [**INFORMACIÓN \_ DE PIN DE \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contiene información que se usa para la autenticación a través de PIN.                                                                            |
| [**INFORMACIÓN \_ DE RADIO BLUETOOTH \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contiene información acerca de una Bluetooth radio.                                                                                    |
| [**BLUETOOTH \_ SELECT \_ DEVICE \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Facilita y administra la visibilidad, la autenticación y la selección de Bluetooth dispositivos y servicios.                         |
| [**BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Almacena información sobre un Bluetooth dispositivo.                                                                                     |
| [**BTH \_ HCI \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Se usa en conexión con la obtención de mensajes DEVICECHANGE de WM \_ para Bluetooth.                                                       |
| [**BTH \_ L2CAP \_ EVENT \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contiene datos sobre los eventos asociados a un canal L2CAP.                                                        |
| [**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Se usa al consultar la presencia de un Bluetooth dispositivo.                                                                       |
| [**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Se usa para consultar un Bluetooth de consulta.                                                                                               |
| [**BTH \_ RADIO \_ IN \_ RANGE**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Almacena datos sobre el Bluetooth dispositivos que están dentro del intervalo de comunicación.                                                     |
| [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Proporciona información de servicio para el servicio Bluetooth especificado.                                                                |
| [**DATOS DEL ELEMENTO SDP \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Almacena datos de elementos SDP.                                                                                                         |
| [**DATOS DE TIPO \_ DE \_ CADENA DE \_ SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Almacena información sobre los tipos de cadena de SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Se usa en una Bluetooth para restringir el conjunto de atributos que se devolverán en la consulta.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilita la búsqueda de UUID.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contiene el UUID en el que se va a realizar una consulta SDP. Se usa junto con la [**estructura SdpQueryUuid.**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Se usa junto con Bluetooth de socket tal como se define en la familia \_ de direcciones BTH de AF.                                   |



 

 

 




