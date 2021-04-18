---
title: TEXT. hoverFontStyle
description: El atributo hoverFontStyle especifica o recupera el estilo de fuente utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Media Player de Windows TEXT. hoverFontStyle
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649642"
---
# <a name="texthoverfontstyle"></a>TEXT. hoverFontStyle

El atributo **hoverFontStyle** especifica o recupera el estilo de fuente utilizado para el control de texto cuando el cursor del mouse se desplaza sobre él.

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción           |
|-----------|-----------------------|
| Bold      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tacha | Estilo de fuente de tachado. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de valores, separados por espacios. El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.

Si no se especifica **hoverFontStyle** , se usa **fontStyle** .

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





