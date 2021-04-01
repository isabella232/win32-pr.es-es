---
title: RegistrationInfo.Docpropiedad umentation
description: En el caso de scripting, obtiene o establece cualquier documentación adicional para la tarea.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Propiedad de documentación Programador de tareas
- Propiedad Documentation Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149865"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Docpropiedad umentation

En el caso de scripting, obtiene o establece cualquier documentación adicional para la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Valor de propiedad

Cualquier documentación adicional que esté asociada a la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, se especifica la documentación adicional para la tarea mediante el elemento [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) del esquema de programador de tareas.

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

 

 





