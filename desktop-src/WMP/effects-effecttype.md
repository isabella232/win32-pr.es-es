---
title: EFFECTs. effectType
description: El método effectType recupera el nombre del registro de la visualización con el índice del registro especificado. Este nombre es un identificador único definido por el autor de la visualización.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699700"
---
# <a name="effectseffecttype"></a>EFFECTs. effectType

El método **effectType** recupera el nombre del registro de la visualización con el índice del registro especificado. Este nombre es un identificador único definido por el autor de la visualización.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número** (**largo**) que contiene el índice del registro de una visualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Este método es útil para cambiar entre visualizaciones en el script. Una interfaz de usuario podría mostrar el conjunto de títulos, pero cuando el usuario selecciona uno, el script debe usar **currentEffectType** para cambiar las visualizaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





