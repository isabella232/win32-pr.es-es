---
title: EFFECTS.currentEffectType
description: El atributo currentEffectType especifica o recupera el nombre del Registro de la visualización actual. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTS.currentEffectType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996755"
---
# <a name="effectscurrenteffecttype"></a>EFFECTS.currentEffectType

El **atributo currentEffectType** especifica o recupera el nombre del Registro de la visualización actual. Este nombre es un identificador único definido por el autor de la visualización.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de lectura **y escritura.**

## <a name="remarks"></a>Comentarios

Puede usar este atributo en tiempo de ejecución para cambiar el efecto mostrado actualmente. Para ello, realice los pasos siguientes:

1.  Use **effectCount** para recuperar el recuento de efectos registrados.
2.  En un bucle, recupere el nombre de cada efecto registrado mediante **effectType**.
3.  Especifique uno de los nombres que recuperó para **currentEffectType** para establecer el efecto actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTS.effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTS.effectType**](effects-effecttype.md)
</dt> </dl>

 

 





