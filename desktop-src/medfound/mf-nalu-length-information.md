---
description: Indica las longitudes de las NALUs en el ejemplo. Se trata de un BLOB MF que se establece en muestras de entrada comprimidas en el descodificador H.264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2020c0086247adda742ce2613045bb3a2004c3b8c13c7cdcb04a0ff3997cf0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104421"
---
# <a name="mf_nalu_length_information-attribute"></a>Atributo MF \_ NALU \_ LENGTH \_ INFORMATION

Indica las longitudes de las NALUs en el ejemplo. Se trata de un **BLOB** MF que se establece en muestras de entrada comprimidas en el descodificador H.264.

## <a name="data-type"></a>Tipo de datos

**Blob**

## <a name="remarks"></a>Comentarios

Para que se establezca este atributo, el medio debe ser de tipo MEDIASUBTYPE H264 y el atributo MF NALU LENGTH SET debe establecerse en el tipo de medio de entrada \_ MEDIASUBTYPE [ \_ \_ \_ ](mf-nalu-length-set.md) \_ H264.

Establezca MF NALU LENGTH INFORMATION como BLOB en el ejemplo de entrada, con \_ \_ un \_ DWORD para cada NALU en el ejemplo.  Por ejemplo, si hay AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), SEGMENTO DE IDR1 (50 k), Segmento 2 de IDR (60 k), debe haber 5 DWORD con los valores 9, 25, 10, 50 k, 60 k en **el BLOB.**

Aquí hay código que establece **blob**, donde **rgdwNCULOLengthInfo** es una matriz de tipo DWORD y **uiNcelaLengthIdx** es las longitudes naLU válidas establecidas en **blob.**


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




