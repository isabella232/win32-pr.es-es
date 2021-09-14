---
title: TEXT.toolTip
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
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374299"
---
# <a name="texttooltip"></a>TEXT.toolTip

El **atributo toolTip** especifica o recupera el texto de información sobre herramientas para el control de texto.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura con una longitud máxima de 1024 caracteres. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Si no se especifica este atributo y  el texto del atributo value se trunca en el control Text o **wordWrap** se establece en true, la información sobre herramientas mostrará el texto completo del atributo **value.**

Cuando este atributo se establece en "" (cadena vacía), no se muestra información sobre herramientas.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





