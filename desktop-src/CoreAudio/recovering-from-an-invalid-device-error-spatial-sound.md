---
description: Recuperación de un error de Invalid-Device (sonido espacial)
title: Recuperación de un error de Invalid-Device (sonido espacial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153399"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Recuperación de un error de Invalid-Device (sonido espacial)

Muchos de los métodos de la API de audio espacial de Microsoft, como [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)y [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), devuelven códigos de error si el dispositivo de punto de conexión de audio que utiliza la aplicación cliente deja de ser válido o se cambia el formato de representación de audio espacial en el extremo. Estos códigos de error indican que el dispositivo de punto de conexión se ha desconectado, o que el hardware de audio o los recursos de hardware asociados se han reconfigurado, deshabilitado, quitado, el modo de audio espacial cambia o no está disponible para su uso. Con frecuencia, la aplicación puede recuperarse de este error.

Los códigos de error que indican un error de dispositivo no válido incluyen los siguientes:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Estrategias para el control de errores de dispositivo no válidos

La estrategia recomendada para recuperarse de un error de dispositivo no válido depende de si la aplicación selecciona automáticamente un dispositivo específico según los requisitos internos o permite al usuario seleccionar explícitamente un dispositivo en una lista de dispositivos disponibles. 

### <a name="default-audio-device"></a>Dispositivo de audio predeterminado

Si la aplicación selecciona automáticamente el dispositivo predeterminado, siga estos pasos para realizar la recuperación.

1. Libere la interfaz [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) y [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) y las demás interfaces de audio espacial que se usen para la representación. 
1. Llame a [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener el dispositivo de audio predeterminado actual.
1. Intente activar **ISpatialAudioClient** en el dispositivo de audio.
1. Active **ISpatialAudioObjectRenderStream**. 

### <a name="specifically-selected-audio-device"></a>Dispositivo de audio seleccionado específicamente

Si la aplicación selecciona un dispositivo de audio específico, siga estos pasos para realizar la recuperación.

1. Libere la interfaz ISpatialAudioObjectRenderStream y cualquier otra interfaz de audio espacial que se use para la representación, pero no publique **ISpatialAudioClient**.
1. Use la instancia actual de **ISpatialAudioClient** para activar **ISpatialAudioObjectRenderStream**.

Tenga en cuenta que para ambas estrategias mencionadas anteriormente, se pueden aplicar los mismos pasos a las aplicaciones que usan las interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) . Simplemente reemplace **ISpatialAudioObjectRenderStream** en los pasos anteriores con las interfaces Metadata o HRTF.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>
[Recuperación de un error](recovering-from-an-invalid-device-error.md) 
 de Invalid-Device [Administración de flujos](stream-management.md)
</dt> </dl>

 

 



