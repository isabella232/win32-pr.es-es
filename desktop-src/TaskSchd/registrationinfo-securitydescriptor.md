---
title: RegistrationInfo. SecurityDescriptor (propiedad)
description: En el caso de scripting, obtiene o establece el descriptor de seguridad de la tarea.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propiedad SecurityDescriptor Programador de tareas
- Propiedad SecurityDescriptor Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685840"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo. SecurityDescriptor (propiedad)

En el caso de scripting, obtiene o establece el descriptor de seguridad de la tarea. Si se proporciona un descriptor de seguridad diferente durante el registro de la tarea, reemplazará el conjunto de descriptores de seguridad por esta propiedad.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valor de propiedad

Descriptor de seguridad asociado a la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el descriptor de seguridad de la tarea se especifica mediante el elemento [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) del esquema de programador de tareas.

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

 

 





