---
title: Objeto de registro de dispositivos
description: Objeto de registro de dispositivos
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- SDK de Windows Media Format, objetos de registro de dispositivos
- Advanced Systems Format (ASF), objetos de registro de dispositivos
- ASF (formato de sistemas avanzados), objetos de registro de dispositivos
- objetos, objetos de registro de dispositivos
- objetos de registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695540"
---
# <a name="device-registration-object"></a>Objeto de registro de dispositivos

El objeto de registro de dispositivos administra la base de datos de registro de dispositivos. Esta base de datos almacena información acerca de los dispositivos de red, como reproductores de vídeo Set-Top, que están conectados al equipo cliente. El propósito principal de la base de datos de registro de dispositivos es administrar los dispositivos que usan el protocolo DRM 10 de Windows Media para dispositivos de red para recibir flujos de datos protegidos.

Si la aplicación admite Windows Media DRM 10 para dispositivos de red, debe usar las interfaces de este objeto para registrar los dispositivos de red y para validar dichos dispositivos. También puede usar la base de datos de registro de dispositivos para almacenar información acerca de los dispositivos de red que no usan Windows Media DRM 10 para dispositivos de red, aunque no toda la información de la base de datos se aplicará a dichos dispositivos.

La función [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) crea el objeto de registro de dispositivos, que establece un puntero a una interfaz **IWMDeviceRegistration** . Los otros métodos del objeto de registro de dispositivos se pueden obtener llamando al método **QueryInterface** .

El objeto de registro de dispositivos admite las siguientes interfaces.



| Interfaz                                              | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Administra la base de datos de registro de dispositivos. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analiza los mensajes enviados por los dispositivos.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Administra la validación del dispositivo.                |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para poder usar los métodos de la interfaz **IWMProximityDetection** .



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de los procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




