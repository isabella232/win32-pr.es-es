---
description: 'MFPKEY_COMPLEXITY propiedad : especifica la complejidad del algoritmo del codificador.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092943"
---
# <a name="mfpkey_complexity-property"></a>Propiedad MFPKEY \_ COMPLEXITY

\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use **MFPKEY \_ COMPLEXITYEX**.\]

Especifica la complejidad del algoritmo del codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

El valor predeterminado depende de la versión del codificador de vídeo, como se muestra en la tabla siguiente.



| Versión del codificador                 | Valor predeterminado |
|---------------------------------|---------------|
| Windows Media Video 9 codificador   | 3             |
| Windows Media Video codificador 7/8 | 1             |



 

## <a name="remarks"></a>Comentarios

Este valor entero oscila entre 0 y 3. Los valores más bajos hacen que el códec use algoritmos de codificación menos complicados. Aunque los algoritmos más sencillos generan resultados de menor calidad, el proceso de codificación es más rápido y requiere menos potencia de procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




