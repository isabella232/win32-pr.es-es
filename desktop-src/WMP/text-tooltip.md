---
title: TEXTO. toolTip
description: El atributo toolTip especifica o recupera el texto de información sobre herramientas para el control de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679505"
---
# <a name="texttooltip"></a>TEXTO. toolTip

El atributo **ToolTip** especifica o recupera el texto de información sobre herramientas para el control de texto.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura con una longitud máxima de 1024 caracteres. No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

Si no se especifica este atributo y el texto del atributo de **valor** se trunca en el control de texto, o el valor de **WordWrap** se establece en true, la información sobre herramientas mostrará el texto completo del atributo **Value** .

Cuando este atributo se establece en "" (cadena vacía), no se muestra ninguna información sobre herramientas.

Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





