---
description: Especifica si el motor de captura usa la aceleración de vídeo de DirectX (DXVA) para lacodización de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580413"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>Atributo DISABLE \_ \_ \_ \_ DXVA de MF CAPTURE ENGINE

Especifica si el motor de captura usa la aceleración de vídeo de DirectX (DXVA) para lacodización de vídeo.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica si se cumplen las condiciones siguientes:

-   El motor de captura descodifica una secuencia de vídeo comprimida del dispositivo de captura (por ejemplo, si el dispositivo de captura genera vídeo H.264).
-   El descodificador de vídeo admite la descodificación acelerada por hardware mediante DXVA.
-   La aplicación usa el [atributo MF CAPTURE ENGINE \_ \_ \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md) para establecer el Administrador de dispositivos DXGI en el motor de captura.

De lo contrario, se omite este atributo.

Este atributo permite que la aplicación deshabilite DXVA mientras se sigue descodando a superficies de Direct3D.

El valor predeterminado de este atributo es **FALSE,** lo que significa que la decodificación de DXVA está habilitada cuando está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




