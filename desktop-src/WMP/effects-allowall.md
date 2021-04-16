---
title: EFFECTs. allowAll
description: El atributo allowAll especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que se encuentran en el registro.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699384"
---
# <a name="effectsallowall"></a>EFFECTs. allowAll

El atributo **allowAll** especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que se encuentran en el registro.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                         |
|-------|---------------------------------------------------------------------|
| true  | Predeterminada. Permite el ciclo de todas las visualizaciones en el sistema del usuario. |
| false | Limita el ciclo a las visualizaciones que aparecen dentro de las etiquetas de **efectos** . |



 

## <a name="remarks"></a>Observaciones

Si este atributo se establece en false, solo las visualizaciones que aparecen dentro de las etiquetas **Effects** se pueden recorrer en iteración mediante PREVIOUS/NEXT. Si se establece en true, todas las visualizaciones que se registran en el sistema del usuario se pueden recorrer. Si se establece en true y se especifican las visualizaciones dentro de las etiquetas **Effects** , los atributos especificados en estas etiquetas se aplican a todas las visualizaciones del sistema del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> </dl>

 

 





