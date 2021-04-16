---
description: Define los algoritmos para el procesador de vídeo que usa el \_ algoritmo del procesador de vídeo MF \_ \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumeración MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696632"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_ \_ \_ Enumeración de tipo de algoritmo del procesador de vídeo MF \_

Define los algoritmos para el procesador de vídeo que usa [el \_ \_ \_ algoritmo del procesador de vídeo MF](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_algoritmo de procesador de vídeo MF \_ \_ \_ predeterminado**
</dt> <dd>

el modo predeterminado favorece un equilibrio de calidad y velocidad

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo del procesador de vídeo MF \_ \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

El procesador de vídeo siempre procesará internamente en AYUV y usará filtros de alta calidad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




