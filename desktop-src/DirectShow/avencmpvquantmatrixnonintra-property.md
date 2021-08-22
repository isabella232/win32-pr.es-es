---
description: Especifica la matriz de cuantificación de luma para los macrobloqueos que no están dentro de . Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 087e47c1-2a8a-4687-85c1-ac18708174e1
title: Propiedad AVEncMPVQuantMatrixNonIntra (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf5898240e2504e3219d419732993b68784fd4c3848ee1928ff1db9262ea02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119258255"
---
# <a name="avencmpvquantmatrixnonintra-property"></a>Propiedad AVEncMPVQuantMatrixNonIntra

Especifica la matriz de cuantificación de luma para los macrobloqueos que no están dentro de . Esta propiedad se aplica a los codificadores de vídeo MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVQuantMatrixNonIntra**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es una cadena que contiene los 64 coeficientes de 8 bits codificados como una cadena de valores hexadecimales (128 caracteres).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




