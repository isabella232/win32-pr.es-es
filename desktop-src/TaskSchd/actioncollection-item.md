---
title: ActionCollection. Item (propiedad)
description: En el caso de scripting, obtiene una acción especificada de la colección.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto ActionCollection
- Programador de tareas de objeto ActionCollection, propiedad Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422490"
---
# <a name="actioncollectionitem-property"></a>ActionCollection. Item (propiedad)

En el caso de scripting, obtiene una acción especificada de la colección.

## <a name="syntax"></a>Sintaxis


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valor de propiedad

Objeto de [**acción**](action.md) que representa la acción solicitada.

## <a name="remarks"></a>Observaciones

Las colecciones se basan en 1. En otras palabras, el índice del primer elemento de la colección es 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





