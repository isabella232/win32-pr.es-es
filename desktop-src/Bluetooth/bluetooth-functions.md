---
title: Bluetooth Funciones
description: Las funciones de esta sección se usan para administrar Bluetooth dispositivos y servicios.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, referencia, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e8d945355b0bc25df4d91a96c30a4d20491eb3b0e86c3542e30c0f2b470833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701415"
---
# <a name="bluetooth-functions"></a>Bluetooth Funciones

Las funciones de esta sección se usan para administrar Bluetooth dispositivos y servicios.

Bluetooth también se admite mediante la interfaz de programación Windows Sockets. Para obtener más información sobre la programación Bluetooth mediante la interfaz Windows Sockets, vea Compatibilidad Windows [sockets](windows-sockets-support-for-bluetooth.md)de Bluetooth .



| Sección                                                                                | Content                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Envía una solicitud de autenticación a un Bluetooth remoto.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Envía una solicitud de autenticación a un Bluetooth remoto. Además, esta función permite que los datos fuera de banda se pasen a la llamada de función para el dispositivo que se autentica. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Permite al autor de la llamada solicitar la autenticación de varios dispositivos durante una única instancia del Asistente para Bluetooth conexión.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Invoca la hoja de propiedades Panel de control información del dispositivo.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Cambia el estado de detección de una red local Bluetooth radios o radios.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Modifica si un servidor local Bluetooth radio acepta conexiones entrantes.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Enumera los GUID (identificadores únicos globales) de los servicios que están habilitados en un Bluetooth dispositivo.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Cierra un identificador de enumeración asociado a una consulta de dispositivo.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Comienza la enumeración de dispositivos Bluetooth locales.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Comienza la enumeración de radios Bluetooth locales.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Busca la siguiente Bluetooth dispositivo.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Busca la siguiente Bluetooth radio.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Cierra el identificador de enumeración asociado a la búsqueda de Bluetooth radios.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Recupera información sobre un dispositivo Bluetooth remoto. El Bluetooth dispositivo debe haber sido identificado previamente a través de una llamada a la función de consulta de dispositivo correcta.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Obtiene información sobre una Bluetooth radio.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Determina si un Bluetooth radio o radios es conectable.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Determina si un Bluetooth radio o radios es reconocible.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registra una función de devolución de llamada a la que se llama cuando un dispositivo Bluetooth solicita autenticación.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registra una aplicación para una solicitud de pin, una comparación numérica y una función de devolución de llamada.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Quita la autenticación entre un Bluetooth y el equipo, purgando cualquier información almacenada en caché sobre el dispositivo.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Enumera a través de la secuencia de registros SDP y llama a la función de devolución de llamada para cada atributo del registro.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Recupera el valor del atributo para un identificador de atributo.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Recorre en iteración una secuencia de contenedor y devuelve cada elemento incluido en el elemento contenedor.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Recupera y analiza un único elemento de una secuencia de SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Convierte una cadena sin formato incrustada en el registro SDP en una cadena Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Habilita Bluetooth selección de dispositivos.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libera los recursos asociados a una llamada anterior a la [**función BluetoothSelectDevices.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Se llama cuando se recibe una solicitud de autenticación para enviar la respuesta de clave de paso.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Se llama cuando se recibe una solicitud de autenticación para enviar la clave de paso o la respuesta de comparación numérica.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Establece la información del servicio local para un Bluetooth radio.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Habilita o deshabilita los servicios de un Bluetooth dispositivo.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Quita el registro de una rutina de devolución de llamada que se registró previamente con una llamada a la [**función BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Actualiza la memoria caché del equipo local sobre Bluetooth dispositivo.                                                                                                                                    |



 

 

 