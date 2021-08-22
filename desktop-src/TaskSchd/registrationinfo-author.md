---
title: RegistrationInfo.Author, propiedad
description: Para el scripting, obtiene o establece el autor de la tarea.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Creación de propiedades Programador de tareas
- Propiedad Author Programador de tareas , objeto RegistrationInfo
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
ms.openlocfilehash: 9a136f41b27f69d95a0817efa24931a994237da90c6c2e0eaf581149687664f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858859"
---
# <a name="registrationinfoauthor-property"></a>RegistrationInfo.Author, propiedad

Para el scripting, obtiene o establece el autor de la tarea.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>Valor de propiedad

Autor de la tarea.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, el autor de la tarea se especifica mediante el [**elemento Author**](taskschedulerschema-author-registrationinfotype-element.md) del Programador de tareas esquema.

Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un recurso .dll archivo. Se usa una cadena especializada para hacer referencia al texto del archivo de recursos. El formato de la cadena es $(@ Dll , ResourceID ), donde Dll es la ruta de acceso al archivo .dll que contiene el recurso y ResourceID es el identificador del texto \[ \] del \[ \] \[ \] \[ \] recurso. Por ejemplo, el establecimiento de este valor de propiedad en $(@ %SystemRoot% \\ System32ResourceName.dll, -101) establecerá la propiedad en el valor del texto del recurso con un identificador igual a -101 en el archivo deResourceName.dll \\ %SystemRoot%. \\ \\

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





