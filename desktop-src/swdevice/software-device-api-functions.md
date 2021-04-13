---
title: Funciones de la API de dispositivo de software
description: En esta sección se describen las funciones de API de dispositivo de software a las que una aplicación cliente llama y una función de devolución de llamada que implementa una aplicación cliente.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a3cc9f0cd8b018f40210c434ee22b3512b2e81
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421301"
---
# <a name="software-device-api-functions"></a>Funciones de la API de dispositivo de software

En esta sección se describen las funciones de API de dispositivo de software a las que una aplicación cliente llama y una función de devolución de llamada que implementa una aplicación cliente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Cierra el identificador de dispositivo de software. Cuando el identificador está cerrado, PnP iniciará el proceso de eliminación del dispositivo.<br/>                                   |
| [**\_devolución de \_ llamada de creación de dispositivo de SW \_**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Proporciona un dispositivo con respaldo en el registro y permite que el llamador realice llamadas a las funciones de la API de dispositivo de software con el identificador *hSwDevice* .<br/> |
| [**SwDeviceCreate**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Inicia la enumeración de un dispositivo de software.<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Obtiene la duración de un dispositivo de software. <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Establece las propiedades de una interfaz de dispositivo de software. <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Registra una interfaz de dispositivo para un dispositivo de software y, opcionalmente, establece las propiedades de esa interfaz. <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Habilita o deshabilita una interfaz de dispositivo para un dispositivo de software. <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Establece las propiedades de un dispositivo de software. <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Administra la duración de un dispositivo de software. <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Libera memoria que otras funciones de la API de dispositivos de software han asignado.<br/>                                                                                      |



 

 

 

[Enviar comentarios acerca de este tema a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Enviar comentarios acerca de este tema a Microsoft")