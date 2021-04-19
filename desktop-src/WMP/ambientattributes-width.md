---
title: AmbientAttributes. width
description: El atributo width especifica o recupera el ancho del control.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes. width Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699342"
---
# <a name="ambientattributeswidth"></a>AmbientAttributes. width

El atributo **width** especifica o recupera el ancho del control.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **entero** de 16 bits de lectura/escritura (de 0 a 32.767) que representa el ancho del control en píxeles. El valor predeterminado es cero o el ancho de la imagen especificada en el atributo de **imagen** del control.

## <a name="remarks"></a>Observaciones

Si el ancho especificado es más estrecho que el ancho de la imagen proporcionada, se recortará la imagen. Si el ancho es más ancho que el ancho de la imagen, la región de clic irá más allá del límite de la imagen. Independientemente del valor que se proporcione a este atributo, la imagen no puede crecer más allá de la **vista** o la **subvista** primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





