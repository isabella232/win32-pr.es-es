---
description: Especifica si el motor de captura utiliza la aceleración de vídeo DirectX (DXVA) para la descodificación de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360386"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Módulo de captura MF \_ \_ deshabilitar el \_ atributo DXVA

Especifica si el motor de captura utiliza la aceleración de vídeo DirectX (DXVA) para la descodificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica si se cumplen las condiciones siguientes:

-   El motor de captura descodifica una secuencia de vídeo comprimida desde el dispositivo de captura (por ejemplo, si el dispositivo de captura emite el vídeo H. 264).
-   El descodificador de vídeo admite la descodificación acelerada por hardware mediante DXVA.
-   La aplicación utiliza el atributo de [Administrador de D3D del \_ motor de captura \_ \_ \_ MF](mf-capture-engine-d3d-manager.md) para establecer la administrador de dispositivos de DXGI en el motor de captura.

De lo contrario, se omite este atributo.

Este atributo permite a la aplicación deshabilitar DXVA mientras se está descodificando en superficies de Direct3D.

El valor predeterminado de este atributo es **false**, lo que significa que la descodificación de DXVA está habilitada cuando está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




