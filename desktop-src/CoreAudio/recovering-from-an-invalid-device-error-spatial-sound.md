---
description: Recuperación de un error Invalid-Device (sonido espacial)
title: Recuperación de un error Invalid-Device (sonido espacial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568573"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Recuperación de un error Invalid-Device (sonido espacial)

Muchos de los métodos de Microsoft Spatial Audio API, como [ISpatialAudioClient,](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject,](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)devuelven códigos de error si el dispositivo de punto de conexión de audio que usa la aplicación cliente deja de ser válido o el formato de representación de audio espacial cambia en el punto de conexión. Estos códigos de error indican que el dispositivo del punto de conexión se ha desconectado o que el hardware de audio o los recursos de hardware asociados se han reconfigurado, deshabilitado, quitado, se ha cambiado el modo de audio espacial o se ha dejado de estar disponible para su uso. Con frecuencia, la aplicación puede recuperarse de este error.

Entre los códigos de error que indican un error de dispositivo no válido se incluyen los siguientes:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Estrategias para controlar errores de dispositivos no válidos

La estrategia recomendada para recuperarse de un error de dispositivo no válido depende de si la aplicación selecciona automáticamente un dispositivo específico en función de los requisitos internos o permite al usuario seleccionar explícitamente un dispositivo de una lista de dispositivos disponibles. 

### <a name="default-audio-device"></a>Dispositivo de audio predeterminado

Si la aplicación selecciona automáticamente el dispositivo predeterminado, siga estos pasos para recuperarlo.

1. Libere las [interfaces ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) y cualquier otra interfaz de audio espacial que se utilice para la representación. 
1. Llame [a IMMDeviceEnumerator::GetDefaultAudioEndpoint para](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) obtener el dispositivo de audio predeterminado actual.
1. Intente activar **ISpatialAudioClient** en el dispositivo de audio.
1. Active **ISpatialAudioObjectRenderStream**. 

### <a name="specifically-selected-audio-device"></a>Dispositivo de audio seleccionado específicamente

Si la aplicación selecciona un dispositivo de audio específico, siga estos pasos para recuperarlo.

1. Libere la interfaz ISpatialAudioObjectRenderStream y cualquier otra interfaz de audio espacial que se utilice para la representación, pero no libere **ISpatialAudioClient.**
1. Use la instancia **actual de ISpatialAudioClient** para activar **ISpatialAudioObjectRenderStream.**

Tenga en cuenta que para ambas estrategias enumeradas anteriormente, se pueden aplicar los mismos pasos a las aplicaciones que usan las interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf.](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) Simplemente reemplace **ISpatialAudioObjectRenderStream** en los pasos anteriores por los metadatos o las interfaces Hrtf.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>
[Recuperación de un error de Invalid-Device](recovering-from-an-invalid-device-error.md) 
 [Administración de flujos](stream-management.md)
</dt> </dl>

 

 



