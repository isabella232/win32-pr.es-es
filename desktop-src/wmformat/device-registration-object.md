---
title: Objeto de registro de dispositivos
description: Objeto de registro de dispositivos
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows SDK de formato multimedia, objetos de registro de dispositivos
- Formato de sistemas avanzados (ASF), objetos de registro de dispositivos
- ASF (formato de sistemas avanzados), objetos de registro de dispositivos
- objects,device registration objects
- objetos de registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360227"
---
# <a name="device-registration-object"></a>Objeto de registro de dispositivos

El objeto de registro de dispositivos administra la base de datos de registro de dispositivos. Esta base de datos almacena información sobre los dispositivos de red, como los reproductores de vídeo de nivel superior establecidos, que están conectados al equipo cliente. El propósito principal de la base de datos de registro de dispositivos es administrar los dispositivos que usan Windows Media DRM 10 para el protocolo de dispositivos de red para recibir flujos de datos protegidos.

Si la aplicación admite Windows Drm multimedia 10 para dispositivos de red, debe usar las interfaces de este objeto para registrar dispositivos de red y validar esos dispositivos. También puede usar la base de datos de registro de dispositivos para almacenar información sobre los dispositivos de red que no usan Windows Media DRM 10 para dispositivos de red, aunque no toda la información de la base de datos se aplicará a dichos dispositivos.

La función [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) crea el objeto de registro del dispositivo, que establece un puntero a una **interfaz IWMDeviceRegistration.** Los demás métodos del objeto de registro de dispositivos se pueden obtener llamando al **método QueryInterface.**

El objeto de registro de dispositivos admite las interfaces siguientes.



| Interfaz                                              | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Administra la base de datos de registro de dispositivos. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analiza los mensajes enviados por los dispositivos.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Administra la validación de dispositivos.                |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para usar los métodos de la **interfaz IWMProximityDetection.**



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




