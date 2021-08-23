---
title: Realizar la detección de proximidad
description: Realizar la detección de proximidad
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows SDK de formato multimedia, realizar la detección de proximidad
- Windows SDK de formato multimedia, detección de proximidad
- Formato de sistemas avanzados (ASF), realizar la detección de proximidad
- ASF (formato de sistemas avanzados), realizar la detección de proximidad
- Formato de sistemas avanzados (ASF), detección de proximidad
- ASF (formato de sistemas avanzados), detección de proximidad
- administración de derechos digitales (DRM), realizar la detección de proximidad
- DRM (administración de derechos digitales), realizar la detección de proximidad
- digital rights management (DRM), detección de proximidad
- DRM (administración de derechos digitales), detección de proximidad
- detección de proximidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b13d56e4c2b1fea0da1ff761f6d915680ff89c42747b9faf4260184ae4205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963984"
---
# <a name="performing-proximity-detection"></a>Realizar la detección de proximidad

Para poder transmitir datos cifrados a un dispositivo registrado en el protocolo DRM 10 de Windows Media para dispositivos de red, debe realizar un proceso denominado detección de proximidad (también denominado validación). Este proceso implica el envío de mensajes al dispositivo y la recepción de respuestas. El tiempo necesario para recibir una respuesta se usa para determinar si el dispositivo está lo suficientemente cerca del equipo de la red para recibir datos seguros. Confirmar que el dispositivo está físicamente cerca del equipo cliente de la red ayuda a evitar la suplantación de seguridad y otros accesos no autorizados.

Cuando la detección de proximidad se completa correctamente, se dice que el dispositivo es válido. Puede comprobar si un dispositivo es válido llamando al [**método IWMRegisteredDevice::IsValid.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) Los dispositivos deben validarse cada 48 horas. Un dispositivo que se validó más de 48 horas antes de que se ejecute el programa debe volver a validarse realizando el proceso de detección de proximidad de nuevo.

Para realizar la detección de proximidad, debe establecer comunicaciones con el dispositivo y, a continuación, llamar al método [**IWMProximityDetection::StartDetection.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) El proceso de detección lo completan de forma asincrónica los componentes drm internos del SDK Windows Media Format. La aplicación debe incluir una implementación de la [**interfaz IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para procesar los mensajes de detección de proximidad.

Hay dos mensajes enviados por el proceso de detección de proximidad: un mensaje de resultado y un mensaje de finalización.

El mensaje de resultado, WMT \_ PROXIMITY \_ RESULT, se envía cuando se completa el proceso de detección. El *parámetro hr* del método de devolución de llamada [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica si se ha encontrado que el dispositivo está lo suficientemente cerca del equipo cliente. Si el *parámetro hr* del mensaje de resultado indica correcto, el parámetro *pValue* contiene un **DWORD** que especifica la latencia medida para el dispositivo en milisegundos.

El mensaje de finalización, WMT \_ PROXIMITY \_ COMPLETED, se envía cuando finaliza la detección. Debe liberar la [**interfaz IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) solo después de recibir este mensaje.

Cuando la detección de proximidad de un dispositivo se realiza correctamente, la base de datos de registro de dispositivos se actualiza automáticamente. Las llamadas posteriores [**a IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) **devolverán TRUE** hasta que transcurran 48 horas y es necesario volver a validar el dispositivo.

**Nota** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de drm Windows multimedia 10 para el protocolo de dispositivos de red**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




