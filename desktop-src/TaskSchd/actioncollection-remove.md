---
title: Método ActionCollection.Remove
description: Para el scripting, quita la acción especificada de la colección.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Quitar método Programador de tareas
- Remove method Programador de tareas , ActionCollection object
- ActionCollection object Programador de tareas , Remove (método)
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011745"
---
# <a name="actioncollectionremove-method"></a>Método ActionCollection.Remove

Para el scripting, quita la acción especificada de la colección.

## <a name="syntax"></a>Sintaxis


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice de la acción que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al quitar elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y que el índice del último elemento es el valor de la [**propiedad ActionCollection.Count.**](actioncollection-count.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





