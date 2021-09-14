---
title: RegistrationInfo.Author, propiedad
description: Para el scripting, obtiene o establece el autor de la tarea.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Creación de propiedades Programador de tareas
- Propiedad Author Programador de tareas objeto , RegistrationInfo
- Objeto RegistrationInfo Programador de tareas , propiedad Author
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172917"
---
# <a name="registrationinfoauthor-property"></a>RegistrationInfo.Author, propiedad

Para el scripting, obtiene o establece el autor de la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>Valor de propiedad

Autor de la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el autor de la tarea se especifica mediante el [**elemento Author**](taskschedulerschema-author-registrationinfotype-element.md) del esquema Programador de tareas tarea.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ \\ %SystemRoot% \\ \\ System32.

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

 

 





