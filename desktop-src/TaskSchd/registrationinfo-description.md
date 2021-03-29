---
title: RegistrationInfo. Description (propiedad)
description: En el caso de scripting, obtiene o establece la descripción de la tarea.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Propiedad Description Programador de tareas
- Propiedad Description Programador de tareas, objeto RegistrationInfo
- Programador de tareas objeto RegistrationInfo, propiedad Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421895"
---
# <a name="registrationinfodescription-property"></a>RegistrationInfo. Description (propiedad)

En el caso de scripting, obtiene o establece la descripción de la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Valor de propiedad

Descripción de la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, la descripción de la tarea se especifica mediante el elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) del esquema de programador de tareas.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll. Una cadena especializada se usa para hacer referencia al texto del archivo de recursos. El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso. Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.

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

 

 





