---
description: Especifica la complejidad del algoritmo del codificador.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Propiedad MFPKEY_COMPLEXITYEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276334"
---
# <a name="mfpkey_complexityex-property"></a>\_Propiedad COMPLEXITYEX de MFPKEY

Especifica la complejidad del algoritmo del codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

El valor predeterminado depende de la versión del codificador de vídeo, tal como se muestra en la tabla siguiente.



| Versión del codificador                 | Valor predeterminado |
|---------------------------------|---------------|
| Codificador de Windows Media Video 9   | 3             |
| Codificador Windows Media Video 7/8 | 1             |



 

## <a name="possible-values"></a>Valores posibles

Los valores posibles dependen de la versión del codificador de vídeo, tal como se muestra en la tabla siguiente.



| Versión del codificador                 | Valores posibles  |
|---------------------------------|------------------|
| Codificador de Windows Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Codificador Windows Media Video 7/8 | 0, 1             |



 

## <a name="remarks"></a>Observaciones

Los valores inferiores hacen que el códec use algoritmos de codificación menos complicados. Aunque los algoritmos más simples producen una salida de menor calidad, el proceso de codificación es más rápido y requiere menos capacidad de procesamiento. Esto puede ser importante al codificar el contenido de un origen en directo porque el codificador debe procesar las entradas lo suficientemente rápido como para mantenerse al día.

Cualquier valor asignado a esta propiedad se omitirá si la propiedad [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) está establecida en 1. En ese caso, MFPKEY \_ COMPLEXITYEX se establece automáticamente en 3.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




