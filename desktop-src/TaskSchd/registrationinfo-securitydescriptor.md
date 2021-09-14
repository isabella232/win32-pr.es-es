---
title: RegistrationInfo.SecurityDescriptor, propiedad
description: Para el scripting, obtiene o establece el descriptor de seguridad de la tarea.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propiedad SecurityDescriptor Programador de tareas
- Propiedad SecurityDescriptor Programador de tareas , objeto RegistrationInfo
- Objeto RegistrationInfo Programador de tareas , propiedad SecurityDescriptor
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172901"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo.SecurityDescriptor, propiedad

Para el scripting, obtiene o establece el descriptor de seguridad de la tarea. Si se proporciona un descriptor de seguridad diferente durante el registro de tareas, sustituirá el descriptor de seguridad establecido con esta propiedad.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valor de propiedad

Descriptor de seguridad asociado a la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el descriptor de seguridad de la tarea se especifica mediante el [**elemento SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) del Programador de tareas esquema.

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
</dt> </dl>

 

 





