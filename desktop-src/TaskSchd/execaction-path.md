---
title: ExecAction. Path (propiedad)
description: En el caso de scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Propiedad path Programador de tareas
- Propiedad path Programador de tareas, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad path
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
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801795"
---
# <a name="execactionpath-property"></a>ExecAction. Path (propiedad)

En el caso de scripting, obtiene o establece la ruta de acceso a un archivo ejecutable.

## <a name="syntax"></a>Sintaxis


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso al archivo ejecutable que va a ejecutar la acción.

## <a name="remarks"></a>Observaciones

Esta acción realiza una operación de línea de comandos. Por ejemplo, la acción podría ejecutar un script o iniciar un ejecutable.

Al leer o escribir XML, la ruta de acceso de la operación de línea de comandos se especifica en el elemento [**Command**](taskschedulerschema-command-exectype-element.md) del esquema programador de tareas.

La ruta de acceso se comprueba para asegurarse de que es válida cuando se registra la tarea, no cuando se establece esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





