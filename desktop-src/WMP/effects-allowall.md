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
ms.openlocfilehash: c7a87aa8336e3961b31716c8d6bbfaa6aee71374a0f3c6e17b644a47136df550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996855"
---
# <a name="effectsallowall"></a>EFFECTS.allowAll

El **atributo allowAll** especifica o recupera un valor que indica si se deben incluir todas las visualizaciones que están en el Registro.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                                                         |
|-------|---------------------------------------------------------------------|
| true  | Predeterminada. Permite el ciclo de todas las visualizaciones en el sistema del usuario. |
| false | Limita el ciclo a las visualizaciones que aparecen dentro de **las etiquetas EFFECTS.** |



 

## <a name="remarks"></a>Comentarios

Si este atributo se establece en false, solo las visualizaciones que aparecen en las etiquetas **EFFECTS** se pueden recorrer en ciclo mediante anterior o siguiente. Si se establece en true, se puede recorrer en ciclo todas las visualizaciones registradas en el sistema del usuario. Si se establece en true y especifica las visualizaciones dentro de etiquetas **EFFECTS,** los atributos especificados en estas etiquetas se aplican a todas las visualizaciones del sistema del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTS, elemento**](effects-element.md)
</dt> </dl>

 

 





