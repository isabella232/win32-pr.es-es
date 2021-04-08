---
title: ExecAction. arguments (propiedad)
description: En el caso de scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments (propiedad) Programador de tareas
- Propiedad arguments Programador de tareas, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996161"
---
# <a name="execactionarguments-property"></a>ExecAction. arguments (propiedad)

En el caso de scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.

## <a name="syntax"></a>Sintaxis


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valor de propiedad

Argumentos necesarios para la operación de la línea de comandos.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML, los argumentos de la operación de línea de comandos se especifican en el elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) del esquema programador de tareas.

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

 

 





