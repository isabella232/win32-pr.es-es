---
title: AmbientAttributes.visible
description: El atributo visible especifica o recupera la visibilidad del control.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes.visible Reproductor de Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889913"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes.visible

El **atributo visible** especifica o recupera la visibilidad del control.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                      |
|-------|----------------------------------|
| true  | Predeterminada. El control está visible. |
| false | El control no se puede ver.      |



 

## <a name="remarks"></a>Observaciones

Este atributo es útil para ocultar controles, por ejemplo, al intercambiar un botón de pausa por un botón de reproducción.

Si el valor es false, el control no está visible y los eventos de clic se pasan al control subyacente. Si el valor es true, el control está visible y recibe el propio evento click.

El valor predeterminado del **elemento AUTOMENU** es false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos ambientales**](ambient-attributes.md)
</dt> </dl>

 

 





