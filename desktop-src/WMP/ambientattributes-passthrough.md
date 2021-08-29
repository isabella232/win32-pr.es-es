---
title: AmbientAttributes.passThrough
description: El atributo passThrough especifica o recupera un valor que indica si el control pasará todos los eventos del mouse al control bajo él.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes.passThrough Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e71e9f7a56f7aa103e64ce739c34467f64cde2edb213c37d2d452b506dc5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055021"
---
# <a name="ambientattributespassthrough"></a>AmbientAttributes.passThrough

El **atributo passThrough** especifica o recupera un valor que indica si el control pasará todos los eventos del mouse al control bajo él.

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Valor | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | El control pasa eventos al control bajo él. |
| false | Predeterminada. El control no pasa eventos a través de .         |



 

## <a name="remarks"></a>Comentarios

Este atributo es útil si, por ejemplo, un control de texto se encuentra encima de un control de botón solo para proporcionar etiquetado. En este caso, los clics en el control de texto se deben pasar al control de botón.

Los elementos **VIEW,** **SUBVIEW** y **PLAYLIST** no admiten el atributo **passThrough.** No funcionará con el elemento **VIDEO** si *VIDEO*. **windowless** se establece en false, ni con el **elemento EFFECTS** si *EFFECTS*. **windowed** se establece en true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





