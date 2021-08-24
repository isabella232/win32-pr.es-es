---
title: TEXT.disabledFontStyle
description: El atributo disabledFontStyle especifica o recupera el estilo de fuente utilizado para el control Text cuando está deshabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- TEXT.disabledFontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0119139e481eee6673c61f95425eac0a3918d738c3d18278442ba7713718b7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507595"
---
# <a name="textdisabledfontstyle"></a>TEXT.disabledFontStyle

El **atributo disabledFontStyle** especifica o recupera el estilo de fuente utilizado para el control Text cuando está deshabilitado.

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno o varios de los valores siguientes.



| Valor     | Descripción           |
|-----------|-----------------------|
| Negrita      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tachado | Estilo de fuente de tachón. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Comentarios

Se puede usar cualquier combinación de los valores, separados por espacios. El estilo Normal tiene prioridad sobre todos los demás valores y se omitirán los demás especificados junto con Normal.

Si **no se especifica disabledFontStyle,** se usa **fontStyle.**

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





