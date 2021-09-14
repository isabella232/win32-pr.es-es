---
description: Define algoritmos para el procesador de vídeo que utiliza MF \_ VIDEO \_ PROCESSOR \_ ALGORITHM.
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE enumeración
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363879"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>ENUMERACIÓN MF \_ VIDEO \_ PROCESSOR ALGORITHM \_ \_ TYPE

Define algoritmos para el procesador de vídeo que utiliza [MF \_ VIDEO PROCESSOR \_ \_ ALGORITHM](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**VALOR \_ PREDETERMINADO DEL ALGORITMO DEL PROCESADOR DE VÍDEO \_ \_ MF \_**
</dt> <dd>

el modo predeterminado favorece un equilibrio de calidad y velocidad

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**ALGORITMO \_ DE PROCESADOR DE VÍDEO MF \_ \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

El procesador de vídeo siempre se procesará internamente en AYUV y usará filtros de alta calidad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| IDL<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation enumeraciones](media-foundation-enumerations.md)
</dt> </dl>

 

 




