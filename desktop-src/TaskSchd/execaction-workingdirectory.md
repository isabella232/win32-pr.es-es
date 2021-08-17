---
title: Propiedad ExecAction.WorkingDirectory
description: Para el scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos que usa el archivo ejecutable.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Propiedad WorkingDirectory Programador de tareas
- Propiedad WorkingDirectory Programador de tareas , objeto ExecAction
- Objeto ExecAction Programador de tareas , propiedad WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139448"
---
# <a name="execactionworkingdirectory-property"></a>Propiedad ExecAction.WorkingDirectory

Para el scripting, obtiene o establece el directorio que contiene el archivo ejecutable o los archivos que usa el archivo ejecutable.

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valor de propiedad

Directorio que contiene el archivo ejecutable o los archivos que usa el archivo ejecutable.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML, el directorio de trabajo de la aplicación se especifica en el [**elemento WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) del Programador de tareas esquema.

La ruta de acceso se comprueba para asegurarse de que es válida cuando se registra la tarea, no cuando se establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





