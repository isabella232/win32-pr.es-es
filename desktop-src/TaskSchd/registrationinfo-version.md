---
title: RegistrationInfo. version (propiedad)
description: En el caso de scripting, obtiene o establece el número de versión de la tarea.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Propiedad versión Programador de tareas
- Propiedad version Programador de tareas, objeto RegistrationInfo
- Objeto RegistrationInfo Programador de tareas, propiedad version
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c312878383c5361317a765cbf84a503244c188a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079048"
---
# <a name="registrationinfoversion-property"></a>RegistrationInfo. version (propiedad)

En el caso de scripting, obtiene o establece el número de versión de la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Valor de propiedad

Número de versión de la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el número de versión de la tarea se especifica utilizando el elemento [**version**](taskschedulerschema-version-registrationinfotype-element.md) del esquema programador de tareas.

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
</dt> </dl>

 

 





