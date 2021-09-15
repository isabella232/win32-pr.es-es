---
title: TEXT.fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control Text.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT.fontStyle Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474566"
---
# <a name="textfontstyle"></a>TEXT.fontStyle

El **atributo fontStyle** especifica o recupera el estilo de fuente para el control Text.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción                 |
|-----------|-----------------------------|
| Negrita      | Estilo de fuente en negrita.            |
| Cursiva    | Estilo de fuente cursiva.          |
| Subrayado | Estilo de fuente de subrayado.       |
| Tachado | Estilo de fuente de tachón.       |
| Normal    | Predeterminada. Estilo de fuente normal. |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de los valores, separados por espacios. El estilo Normal tiene prioridad sobre todos los demás valores y se omitirán los demás especificados junto con Normal.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





