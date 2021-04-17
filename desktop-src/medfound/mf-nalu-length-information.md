---
description: Indica las longitudes de NALUs en el ejemplo. Se trata de un BLOB MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697024"
---
# <a name="mf_nalu_length_information-attribute"></a>MF \_ Nalu \_ atributo de información de longitud \_

Indica las longitudes de NALUs en el ejemplo. Se trata de un **BLOB** MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 264.

## <a name="data-type"></a>Tipo de datos

**BLOB**

## <a name="remarks"></a>Observaciones

Para que se establezca este atributo, el medio debe ser de tipo MEDIASUBTYPE \_ H264 y el atributo de [ \_ conjunto de \_ longitud \_ MF Nalu](mf-nalu-length-set.md) debe establecerse en el tipo de medio de entrada de MEDIASUBTYPE \_ H264.

Establezca la \_ información de longitud de MF Nalu \_ \_ como un **BLOB** en el ejemplo de entrada, con un valor DWORD para cada Nalu en el ejemplo. Por ejemplo, si hay 300 000 (9 bytes), SP (25 bytes), PPS (10 bytes), IDR slice1 (50 k), el segmento de IDR 2 (60 k), debe haber 5 DWORD con los valores 9, 25, 10, 50 k, 60 k en el **BLOB**.

Aquí se muestra código que establece el **BLOB**, donde **rgdwNALULengthInfo** es una matriz de tipo DWORD y **uiNaluLengthIdx** es la longitud Nalu válida establecida en el **BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




