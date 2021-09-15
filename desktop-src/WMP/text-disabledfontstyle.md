---
title: TEXT.disabledFontStyle
description: El atributo disabledFontStyle especifica o recupera el estilo de fuente utilizado para el control Text cuando está deshabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Text.disabledFontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569761"
---
# <a name="textdisabledfontstyle"></a>TEXT.disabledFontStyle

El **atributo disabledFontStyle** especifica o recupera el estilo de fuente utilizado para el control Text cuando está deshabilitado.

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción           |
|-----------|-----------------------|
| Negrita      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tachado | Estilo de fuente de tachón. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de los valores, separados por espacios. El estilo Normal tiene prioridad sobre todos los demás valores y se omitirán los demás especificados junto con Normal.

Si **no se especifica disabledFontStyle,** se usa **fontStyle.**

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





