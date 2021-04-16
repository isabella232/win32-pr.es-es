---
title: TEXT. fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de texto.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649551"
---
# <a name="textfontstyle"></a>TEXT. fontStyle

El atributo **fontStyle** especifica o recupera el estilo de fuente para el control de texto.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción                 |
|-----------|-----------------------------|
| Bold      | Estilo de fuente en negrita.            |
| Cursiva    | Estilo de fuente cursiva.          |
| Subrayado | Estilo de fuente de subrayado.       |
| Tacha | Estilo de fuente de tachado.       |
| Normal    | Predeterminada. Estilo de fuente normal. |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de valores, separados por espacios. El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





