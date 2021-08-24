---
title: Propiedad ActionCollection.Context
description: Para el scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Propiedades de contexto Programador de tareas
- Propiedad context Programador de tareas , objeto ActionCollection
- Objeto ActionCollection Programador de tareas , propiedad Context
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff495e4ef2742a6a05570308f2976c014026941d290d44c39bdd087ce3e13a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772755"
---
# <a name="actioncollectioncontext-property"></a>Propiedad ActionCollection.Context

Para el scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de la entidad de seguridad de la tarea. El identificador que se especifica aquí debe coincidir con el identificador especificado en la propiedad Id de la interfaz IPrincipal que define la entidad de seguridad.

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

 

 





