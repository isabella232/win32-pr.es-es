---
title: EFFECTs. currentEffectType
description: El atributo currentEffectType especifica o recupera el nombre del registro de la visualización actual. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699372"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. currentEffectType

El atributo **currentEffectType** especifica o recupera el nombre del registro de la visualización actual. Este nombre es un identificador único definido por el autor de la visualización.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Puede utilizar este atributo en tiempo de ejecución para cambiar el efecto que se muestra actualmente. Para ello, siga estos pasos:

1.  Use **effectCount** para recuperar el recuento de efectos registrados.
2.  En un bucle, recupere el nombre de cada efecto registrado mediante **effectType**.
3.  Especifique uno de los nombres que recuperó para **currentEffectType** para establecer el efecto actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTs. effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTs. effectType**](effects-effecttype.md)
</dt> </dl>

 

 





