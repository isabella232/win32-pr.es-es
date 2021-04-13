---
description: Especifica la complejidad del algoritmo del codificador.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Propiedad MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276333"
---
# <a name="mfpkey_complexity-property"></a>Propiedad de complejidad de MFPKEY \_

\[[**MFPKEY \_ La complejidad**](mfpkey-complexityexproperty.md) está disponible para su uso en los sistemas operativos especificados en la sección requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use **MFPKEY \_ COMPLEXITYEX**.\]

Especifica la complejidad del algoritmo del codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

El valor predeterminado depende de la versión del codificador de vídeo, tal como se muestra en la tabla siguiente.



| Versión del codificador                 | Valor predeterminado |
|---------------------------------|---------------|
| Codificador de Windows Media Video 9   | 3             |
| Codificador Windows Media Video 7/8 | 1             |



 

## <a name="remarks"></a>Observaciones

Este valor entero va de 0 a 3. Los valores inferiores hacen que el códec use algoritmos de codificación menos complicados. Aunque los algoritmos más simples producen una salida de menor calidad, el proceso de codificación es más rápido y requiere menos capacidad de procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




