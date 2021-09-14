---
title: TEXT.hoverFontStyle
description: El atributo hoverFontStyle especifica o recupera el estilo de fuente utilizado para el control Text cuando el cursor del mouse se desplaza sobre él.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT.hoverFontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170557"
---
# <a name="texthoverfontstyle"></a>TEXT.hoverFontStyle

El **atributo hoverFontStyle** especifica o recupera el estilo de fuente utilizado para el control Text cuando el cursor del mouse se desplaza sobre él.

``` syntax
        elementID.hoverFontStyle
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

Si **no se especifica hoverFontStyle,** se usa **fontStyle.**

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

 

 





