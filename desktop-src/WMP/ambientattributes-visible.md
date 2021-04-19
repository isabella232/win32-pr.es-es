---
title: AmbientAttributes. visible
description: El atributo visible especifica o recupera la visibilidad del control.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes. visible Media Player de Windows
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700095"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes. visible

El atributo **visible** especifica o recupera la visibilidad del control.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                      |
|-------|----------------------------------|
| true  | Predeterminada. El control está visible. |
| false | El control no se puede ver.      |



 

## <a name="remarks"></a>Observaciones

Este atributo es útil para ocultar controles, por ejemplo, al intercambiar un botón de pausa para un botón de reproducción.

Si el valor es false, el control no es visible y los eventos de clic se pasan al control subyacente. Si el valor es true, el control es visible y recibe el propio evento de clic.

El valor predeterminado del elemento de **menú automenu** es false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





