---
title: EFFECTS.allowAll
description: El atributo allowAll especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que están en el Registro.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTS.allowAll Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242541"
---
# <a name="effectsallowall"></a>EFFECTS.allowAll

El **atributo allowAll** especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que están en el Registro.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                                         |
|-------|---------------------------------------------------------------------|
| true  | Predeterminada. Permite el ciclo de todas las visualizaciones en el sistema del usuario. |
| false | Limita el ciclo a las visualizaciones que aparecen en las **etiquetas EFFECTS.** |



 

## <a name="remarks"></a>Observaciones

Si este atributo se establece en false, solo las visualizaciones que aparecen en las etiquetas **EFFECTS** se pueden recorrer mediante el uso de anterior o siguiente. Si se establece en true, todas las visualizaciones registradas en el sistema del usuario se pueden recorrer en ciclo. Si se establece en true y especifica las visualizaciones dentro de las etiquetas **EFFECTS,** los atributos especificados en estas etiquetas se aplican a todas las visualizaciones del sistema del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO EFFECTS**](effects-element.md)
</dt> </dl>

 

 





