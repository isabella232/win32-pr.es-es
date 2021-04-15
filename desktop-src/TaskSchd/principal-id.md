---
title: Propiedad Principal.Id
description: En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Propiedad ID Programador de tareas
- Propiedad ID Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422488"
---
# <a name="principalid-property"></a>Propiedad Principal.Id

En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad.

## <a name="syntax"></a>Sintaxis


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valor de propiedad

El identificador de la entidad de seguridad.

## <a name="remarks"></a>Observaciones

Este identificador también se utiliza al especificar la propiedad [**ActionCollection. Context**](actioncollection-context.md) .

Al leer o escribir XML para una tarea, el identificador de la entidad de seguridad se especifica en el atributo ID del elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





