---
title: Text.toolTip
description: El atributo toolTip especifica o recupera el texto de información sobre herramientas para el control de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- Text.toolTip Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 726337ffb31b86d4eaa3a20a1d922fc622110b647fe9be747e8ae239c4548276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831824"
---
# <a name="texttooltip"></a>Text.toolTip

El **atributo toolTip** especifica o recupera el texto de información sobre herramientas para el control de texto.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura con una longitud máxima de 1024 caracteres. No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Si no se especifica este atributo y el texto del atributo **value** se trunca en el control Text, o **wordWrap** se establece en true, la información sobre herramientas mostrará el texto completo del atributo **value.**

Cuando este atributo se establece en "" (cadena vacía), no se muestra información sobre herramientas.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





