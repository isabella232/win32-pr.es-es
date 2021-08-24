---
description: Especifica si el motor de captura usa la aceleración de vídeo de DirectX (DXVA) para lacodización de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941015"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>Atributo DISABLE \_ \_ \_ \_ DXVA de MF CAPTURE ENGINE

Especifica si el motor de captura usa la aceleración de vídeo de DirectX (DXVA) para lacodización de vídeo.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica si se cumplen las condiciones siguientes:

-   El motor de captura descodifica una secuencia de vídeo comprimida del dispositivo de captura (por ejemplo, si el dispositivo de captura genera vídeo H.264).
-   El descodificador de vídeo admite la descodificación acelerada por hardware mediante DXVA.
-   La aplicación usa el atributo [MF \_ CAPTURE ENGINE \_ \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md) para establecer el Administrador de dispositivos DXGI en el motor de captura.

De lo contrario, se omite este atributo.

Este atributo permite que la aplicación deshabilite DXVA mientras se sigue descodando en superficies de Direct3D.

El valor predeterminado de este atributo es **FALSE,** lo que significa que lacoding dxva está habilitada cuando está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




