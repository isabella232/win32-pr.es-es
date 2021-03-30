---
title: Propiedad RegistrationInfo. Source
description: Para scripting, obtiene o establece el origen desde el que se originó la tarea. Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Propiedad de origen Programador de tareas
- Propiedad Source Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802983"
---
# <a name="registrationinfosource-property"></a>Propiedad RegistrationInfo. Source

Para scripting, obtiene o establece el origen desde el que se originó la tarea. Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valor de propiedad

Donde se originó la tarea. Por ejemplo, de un componente, servicio, aplicación o usuario.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, la información de origen de la tarea se especifica utilizando el elemento de [**origen**](taskschedulerschema-source-registrationinfotype-element.md) del esquema de programador de tareas.

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

 

 





