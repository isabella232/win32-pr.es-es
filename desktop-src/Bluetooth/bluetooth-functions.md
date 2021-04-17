---
title: Funciones de Bluetooth
description: Las funciones de esta sección se usan para administrar dispositivos y servicios Bluetooth.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, referencia, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5343f0d609185f3bb472570b8454931fc6a18b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487783"
---
# <a name="bluetooth-functions"></a>Funciones de Bluetooth

Las funciones de esta sección se usan para administrar dispositivos y servicios Bluetooth.

Bluetooth también es compatible con la interfaz de programación de Windows Sockets. Para obtener más información acerca de la programación de Bluetooth mediante la interfaz de Windows Sockets, consulte [compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sección                                                                                | Contenido                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Envía una solicitud de autenticación a un dispositivo Bluetooth remoto.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Envía una solicitud de autenticación a un dispositivo Bluetooth remoto. Además, esta función permite pasar datos fuera de banda a la llamada de función para el dispositivo que se va a autenticar. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Permite que el autor de la llamada solicite la autenticación de varios dispositivos durante una única instancia del Asistente para conexión Bluetooth.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Invoca la hoja de propiedades información del dispositivo del panel de control.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Cambia el estado de detección de una radio o radio Bluetooth local.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Modifica si una radio Bluetooth local acepta conexiones entrantes.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Enumera los GUID (identificadores únicos globales) de los servicios que están habilitados en un dispositivo Bluetooth.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Cierra un identificador de enumeración que está asociado a una consulta de dispositivo.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Comienza la enumeración de los dispositivos Bluetooth locales.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Comienza la enumeración de las radios Bluetooth locales.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Busca el siguiente dispositivo Bluetooth.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Busca el siguiente radio Bluetooth.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Cierra el identificador de enumeración asociado a la búsqueda de radios Bluetooth.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Recupera información acerca de un dispositivo Bluetooth remoto. El dispositivo Bluetooth debe haberse identificado previamente a través de una llamada de función de consulta de dispositivo correcta.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Obtiene información acerca de una radio Bluetooth.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Determina si un radio o radio Bluetooth es conectable.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Determina si un radio o radio Bluetooth es reconocible.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registra una función de devolución de llamada a la que se llama cuando un dispositivo Bluetooth determinado solicita la autenticación.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registra una aplicación para una solicitud de PIN, una comparación numérica y una función de devolución de llamada.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Quita la autenticación entre un dispositivo Bluetooth y el equipo, y purga cualquier información almacenada en caché sobre el dispositivo.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Enumera a través de la secuencia de registro SDP y llama a la función de devolución de llamada para cada atributo del registro.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Recupera el valor de atributo para un identificador de atributo.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Recorre en iteración una secuencia de contenedor y devuelve todos los elementos contenidos en el elemento contenedor.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Recupera y analiza un solo elemento de una secuencia SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Convierte una cadena sin formato que está incrustada en el registro SDP en una cadena Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Habilita la selección de dispositivos Bluetooth.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libera los recursos asociados a una llamada anterior a la función [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Se le llama cuando se recibe una solicitud de autenticación para enviar la respuesta de clave de paso.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Se llama cuando se recibe una solicitud de autenticación para enviar la clave de paso o la respuesta de comparación numérica.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Establece la información del servicio local para un radio Bluetooth específico.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Habilita o deshabilita los servicios para un dispositivo Bluetooth.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Quita el registro de una rutina de devolución de llamada que se registró previamente con una llamada a la función [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Actualiza la memoria caché del equipo local sobre un dispositivo Bluetooth.                                                                                                                                    |



 

 

 