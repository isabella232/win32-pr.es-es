---
title: Realización de la detección de proximidad
description: Realización de la detección de proximidad
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- SDK de Windows Media Format, realización de detección de proximidad
- SDK de Windows Media Format, detección de proximidad
- Advanced Systems Format (ASF), realizando la detección de proximidad
- ASF (formato de sistemas avanzados), realizando detección de proximidad
- Advanced Systems Format (ASF), detección de proximidad
- ASF (formato de sistemas avanzados), detección de proximidad
- Administración de derechos digitales (DRM), realización de detección de proximidad
- DRM (administración de derechos digitales), realización de la detección de proximidad
- Administración de derechos digitales (DRM), detección de proximidad
- DRM (administración de derechos digitales), detección de proximidad
- detección de proximidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420223"
---
# <a name="performing-proximity-detection"></a>Realización de la detección de proximidad

Antes de poder transmitir datos cifrados a un dispositivo registrado en el protocolo DRM 10 de Windows Media para dispositivos de red, debe realizar un proceso denominado detección de proximidad (también denominado validación). Este proceso implica el envío de mensajes al dispositivo y la recepción de respuestas. El tiempo que se tarda en recibir una respuesta se usa para determinar si el dispositivo está lo suficientemente cerca del equipo en la red para recibir datos seguros. La confirmación de que el dispositivo está físicamente cerca del equipo cliente en la red ayuda a evitar la suplantación de identidad y otro acceso no autorizado.

Cuando la detección de proximidad se completa correctamente, se dice que el dispositivo es válido. Puede comprobar si un dispositivo es válido llamando al método [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) . Los dispositivos deben validarse cada 48 horas. Un dispositivo que se validó más de 48 horas antes de que se ejecute el programa debe volver a validarse realizando de nuevo el proceso de detección de proximidad.

Para realizar la detección de proximidad, debe establecer comunicaciones con el dispositivo y, a continuación, llamar al método [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) . Los componentes de DRM internos del SDK de Windows Media Format completan el proceso de detección de forma asincrónica. La aplicación debe incluir una implementación de la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para procesar los mensajes de detección de proximidad.

Hay dos mensajes que se envían mediante el proceso de detección de proximidad: un mensaje de resultado y un mensaje de finalización.

El mensaje de resultado, el resultado de proximidad de WMT \_ \_ , se envía cuando se completa el proceso de detección. El parámetro *HR* del método de devolución de llamada de [**Estado**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica si el dispositivo se ha encontrado lo suficientemente cerca del equipo cliente. Si el parámetro *HR* del mensaje de resultado indica que la operación se ha realizado correctamente, el parámetro *PValue* contiene un **valor DWORD** que especifica la latencia medida para el dispositivo en milisegundos.

\_ \_ Cuando finaliza la detección, se envía el mensaje de finalización de la proximidad de WMT. Solo debe liberar la interfaz [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) después de recibir este mensaje.

Cuando la detección de proximidad de un dispositivo se realiza correctamente, la base de datos de registro de dispositivos se actualiza automáticamente. Las llamadas subsiguientes a [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) devolverán **true** hasta que hayan transcurrido 48 horas y se deba volver a validar el dispositivo.

**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el protocolo DRM 10 de Windows Media para dispositivos de red**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




