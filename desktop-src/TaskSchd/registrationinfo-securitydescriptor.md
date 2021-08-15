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
ms.openlocfilehash: c5c3aa83bc05952007d9114ad9812068de5b5b0bd82a4ce9e14e4d5ba1025bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759567"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo.SecurityDescriptor, propiedad

Para el scripting, obtiene o establece el descriptor de seguridad de la tarea. Si se proporciona un descriptor de seguridad diferente durante el registro de tareas, sustituirá el descriptor de seguridad establecido con esta propiedad.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valor de propiedad

Descriptor de seguridad asociado a la tarea.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, el descriptor de seguridad de la tarea se especifica mediante el [**elemento SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





