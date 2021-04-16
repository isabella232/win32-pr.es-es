---
title: ActionCollection. Context (propiedad)
description: En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Propiedad de contexto Programador de tareas
- Propiedad de contexto Programador de tareas, objeto ActionCollection
- Programador de tareas de objeto ActionCollection, propiedad de contexto
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
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686088"
---
# <a name="actioncollectioncontext-property"></a>ActionCollection. Context (propiedad)

En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad para la tarea.

## <a name="syntax"></a>Sintaxis


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador de la entidad de seguridad de la tarea. El identificador que se especifica aquí debe coincidir con el identificador especificado en la propiedad ID de la interfaz IPrincipal que define la entidad de seguridad.

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

 

 





