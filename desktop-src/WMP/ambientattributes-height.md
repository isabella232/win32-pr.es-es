---
title: AmbientAttributes. Height
description: El atributo height especifica o recupera el alto del control.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes. Height Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700064"
---
# <a name="ambientattributesheight"></a>AmbientAttributes. Height

El atributo **height** especifica o recupera el alto del control.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (**Long**) que representa el alto del control en píxeles. El valor predeterminado es cero o el alto de la imagen especificada en el atributo de **imagen** del control.

## <a name="remarks"></a>Observaciones

Si el alto especificado es menor que el alto de la imagen proporcionada, se recortará la imagen. Si el alto es mayor que el alto de la imagen, la región de clic irá más allá del límite de la imagen. Independientemente del valor que se proporcione a este atributo, la imagen no puede crecer más allá de la **vista** o la **subvista** primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





