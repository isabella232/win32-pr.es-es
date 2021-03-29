---
title: Estructuras de Bluetooth
description: En esta sección se proporcionan las definiciones de las estructuras utilizadas para administrar dispositivos y servicios Bluetooth.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, referencia, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df10989e41814f6f750bdcc719f01b14ccae315
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903163"
---
# <a name="bluetooth-structures"></a>Estructuras de Bluetooth

En esta sección se proporcionan las definiciones de las estructuras utilizadas para administrar dispositivos y servicios Bluetooth.

Bluetooth también es compatible con la interfaz de programación de Windows Sockets. Para obtener más información acerca de la programación de Bluetooth mediante la interfaz de Windows Sockets, consulte [compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sección                                                                                       | Contenido                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_dirección Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contiene la dirección de un dispositivo Bluetooth.                                                                                      |
| [**\_parámetros de devolución de llamada de autenticación Bluetooth \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contiene información de configuración específica sobre el dispositivo Bluetooth que responde a una solicitud de autenticación.                  |
| [**\_respuesta de autenticación \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contiene información pasada en respuesta a un \_ evento de solicitud de autenticación remota de BTH \_ \_ .                                           |
| [**\_pares de c.o.d. de Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Proporciona la especificación y recuperación de información de clase de dispositivo (COD) Bluetooth.                                         |
| [**\_información del dispositivo Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Proporciona información acerca de un dispositivo Bluetooth.                                                                                   |
| [**\_parámetros de \_ búsqueda de dispositivos Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Especifica los criterios de búsqueda para las búsquedas de dispositivos Bluetooth.                                                                         |
| [**\_parámetros de \_ radio de búsqueda de Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Facilita la enumeración de las radios Bluetooth instaladas.                                                                       |
| [**\_información del \_ servicio \_ local de Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contiene información de servicio local para un radio Bluetooth.                                                                        |
| [**\_información de \_ comparación \_ numérica de Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contiene el valor numérico que se usa para la autenticación a través de una comparación numérica.                                                       |
| [**\_información de \_ datos \_ OOB de Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contiene los datos que se usan para autenticarse antes de establecer un emparejamiento de dispositivos fuera de banda.                                          |
| [**información de clave de paso de BLUETOOTH \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contiene la clave de paso que se usa para la autenticación mediante la clave de paso.                                                                        |
| [**\_información del PIN de Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contiene información usada para la autenticación a través del PIN.                                                                            |
| [**\_información de radio Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contiene información acerca de una radio Bluetooth.                                                                                    |
| [**\_parámetros de selección de \_ dispositivo Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Facilita y administra la visibilidad, la autenticación y la selección de dispositivos y servicios Bluetooth.                         |
| [**\_información del dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Almacena información acerca de un dispositivo Bluetooth.                                                                                     |
| [**BTH \_ \_ información de evento de HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Se usa en conexión con la obtención \_ de mensajes de WM DEVICECHANGE para Bluetooth.                                                       |
| [**BTH \_ \_ información de evento de L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contiene datos sobre los eventos que están asociados a un canal L2CAP.                                                        |
| [**\_dispositivo de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Se usa cuando se consulta la presencia de un dispositivo Bluetooth.                                                                       |
| [**\_servicio de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Se usa para consultar un servicio Bluetooth.                                                                                               |
| [**\_radio BTH \_ en el \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Almacena datos acerca de los dispositivos Bluetooth que se encuentran dentro del intervalo de comunicación.                                                     |
| [**BTH \_ establecer \_ servicio**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Proporciona información del servicio para el servicio Bluetooth especificado.                                                                |
| [**\_datos del elemento SDP \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Almacena los datos de los elementos SDP.                                                                                                         |
| [**\_datos de \_ tipo de cadena SDP \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Almacena información sobre los tipos de cadena SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Se utiliza en una consulta de Bluetooth para restringir el conjunto de atributos que se van a devolver en la consulta.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilita la búsqueda de UUID.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contiene el UUID en el que se va a realizar una consulta SDP. Se usa junto con la estructura [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) . |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Se usa junto con las operaciones de Socket Bluetooth tal y como se define en la \_ familia de direcciones AF BTH.                                   |



 

 

 




