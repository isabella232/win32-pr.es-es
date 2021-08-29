---
title: Propiedad ExecAction.Path
description: Para el scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Ruta de acceso Programador de tareas
- Propiedad Path Programador de tareas , objeto ExecAction
- Objeto ExecAction Programador de tareas , propiedad Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d363485db56634c39a4a12e153feb740b0c21a2b6a3ef9499754de753c6236f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011455"
---
# <a name="execactionpath-property"></a>Propiedad ExecAction.Path

Para el scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso al archivo ejecutable que va a ejecutar la acción.

## <a name="remarks"></a>Comentarios

Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script o iniciar un archivo ejecutable.

Al leer o escribir XML, la ruta de acceso de la operación de línea de comandos se especifica en el elemento [**Command**](taskschedulerschema-command-exectype-element.md) del Programador de tareas esquema.

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

 

 





