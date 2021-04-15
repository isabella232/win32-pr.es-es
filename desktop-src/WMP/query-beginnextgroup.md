---
title: Query. beginNextGroup (método)
description: El método beginNextGroup comienza un nuevo grupo de condiciones. | Query. beginNextGroup (método)
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- método beginNextGroup de Windows Media Player
- método beginNextGroup de Windows Media Player, clase de consulta
- Clase de consulta de Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709070"
---
# <a name="querybeginnextgroup-method"></a>Query. beginNextGroup (método)

El método **beginNextGroup** comienza un nuevo grupo de condiciones.

## <a name="syntax"></a>Sintaxis


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El inicio de un nuevo grupo de condiciones implica que se ha completado el grupo de condiciones actual. El nuevo grupo de condiciones siempre se concatena al grupo de condiciones anterior mediante la lógica o.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Query (objeto)**](query-object.md)
</dt> <dt>

[**Consulta. addCondition**](query-addcondition.md)
</dt> </dl>

 

 





