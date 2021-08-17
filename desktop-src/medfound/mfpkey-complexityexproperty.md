---
description: 'MFPKEY_COMPLEXITYEX propiedad : especifica la complejidad del algoritmo del codificador.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873542"
---
# <a name="mfpkey_complexityex-property"></a>Propiedad MFPKEY \_ COMPLEXITYEX

Especifica la complejidad del algoritmo del codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

El valor predeterminado depende de la versión del codificador de vídeo, como se muestra en la tabla siguiente.



| Versión del codificador                 | Valor predeterminado |
|---------------------------------|---------------|
| Windows Codificador Media Video 9   | 3             |
| Windows Codificador Media Video 7/8 | 1             |



 

## <a name="possible-values"></a>Valores posibles

Los valores posibles dependen de la versión del codificador de vídeo, como se muestra en la tabla siguiente.



| Versión del codificador                 | Valores posibles  |
|---------------------------------|------------------|
| Windows Codificador Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Windows Codificador Media Video 7/8 | 0, 1             |



 

## <a name="remarks"></a>Comentarios

Los valores inferiores hacen que el códec use algoritmos de codificación menos complicados. Aunque los algoritmos más sencillos generan resultados de menor calidad, el proceso de codificación es más rápido y requiere menos potencia de procesamiento. Esto puede ser importante al codificar contenido desde un origen en directo porque el codificador debe procesar las entradas lo suficientemente rápido como para mantenerse al día con el origen.

Cualquier valor asignado a esta propiedad se omitirá si la propiedad [ \_ MFPKEY COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) está establecida en 1. En ese caso, MFPKEY \_ COMPLEXITYEX se establece automáticamente en 3.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




