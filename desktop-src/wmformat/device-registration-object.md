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
ms.openlocfilehash: 4594b17f6824e4e3a9e7690e5ea933e24670e9c8b5d95feb16e555f577f87f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433891"
---
# <a name="device-registration-object"></a>Objeto de registro de dispositivos

El objeto de registro de dispositivos administra la base de datos de registro de dispositivos. Esta base de datos almacena información sobre los dispositivos de red, como los reproductores de vídeo de nivel superior establecidos, que están conectados al equipo cliente. El propósito principal de la base de datos de registro de dispositivos es administrar los dispositivos que usan Windows Media DRM 10 para el protocolo de dispositivos de red para recibir flujos de datos protegidos.

Si la aplicación admite Windows Media DRM 10 para dispositivos de red, debe usar las interfaces de este objeto para registrar dispositivos de red y validar esos dispositivos. También puede usar la base de datos de registro de dispositivos para almacenar información sobre los dispositivos de red que no usan Windows Media DRM 10 para dispositivos de red, aunque no toda la información de la base de datos se aplicará a dichos dispositivos.

La función [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) crea el objeto de registro del dispositivo, que establece un puntero a una **interfaz IWMDeviceRegistration.** Los demás métodos del objeto de registro de dispositivos se pueden obtener llamando al **método QueryInterface.**

El objeto de registro de dispositivos admite las siguientes interfaces.



| Interfaz                                              | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| [**IWMDeviceRegistration**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | Administra la base de datos de registro de dispositivos. |
| [**IWMDRMMessageParser**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | Analiza los mensajes enviados por los dispositivos.          |
| [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | Administra la validación del dispositivo.                |



 

La aplicación debe implementar la siguiente interfaz de devolución de llamada para usar los métodos de la **interfaz IWMProximityDetection.**



| Interfaz                                      | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recibe mensajes de estado de procesos que se ejecutan en un subproceso independiente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objects**](objects.md)
</dt> </dl>

 

 




