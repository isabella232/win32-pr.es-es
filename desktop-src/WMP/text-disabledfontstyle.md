---
title: TEXT. disabledFontStyle
description: El atributo disabledFontStyle especifica o recupera el estilo de fuente utilizado para el control de texto cuando está deshabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Media Player de Windows TEXT. disabledFontStyle
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718821"
---
# <a name="textdisabledfontstyle"></a>TEXT. disabledFontStyle

El atributo **disabledFontStyle** especifica o recupera el estilo de fuente utilizado para el control de texto cuando está deshabilitado.

``` syntax
        elementID.disabledFontStyle
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

Si no se especifica **disabledFontStyle** , se usa **fontStyle** .

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

 

 





