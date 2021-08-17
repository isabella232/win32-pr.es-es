---
title: EFFECTS.effectType
description: El método effectType recupera el nombre del Registro de la visualización con el índice del Registro especificado. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTS.effectType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749237"
---
# <a name="effectseffecttype"></a>EFFECTS.effectType

El **método effectType** recupera el nombre del Registro de la visualización con el índice del Registro especificado. Este nombre es un identificador único definido por el autor de la visualización.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number** (**long**) que contiene el índice del Registro de una visualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Comentarios

Este método es útil para cambiar entre visualizaciones en el script. Una interfaz de usuario podría mostrar el conjunto de títulos, pero cuando el usuario selecciona uno, el script debe usar **currentEffectType** para cambiar las visualizaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTS, elemento**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





