---
title: Método Query.beginNextGroup
description: El método beginNextGroup comienza un nuevo grupo de condiciones. | Método Query.beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Método beginNextGroup Reproductor de Windows Media
- Método beginNextGroup Reproductor de Windows Media , clase Query
- Clase de consulta Reproductor de Windows Media método , beginNextGroup
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070951"
---
# <a name="querybeginnextgroup-method"></a>Método Query.beginNextGroup

El **método beginNextGroup** comienza un nuevo grupo de condiciones.

## <a name="syntax"></a>Sintaxis


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El inicio de un nuevo grupo de condiciones implica que ha completado el grupo de condiciones actual. El nuevo grupo de condiciones siempre se concatena con el grupo de condiciones anterior mediante la lógica OR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> <dt>

[**Query.addCondition**](query-addcondition.md)
</dt> </dl>

 

 





