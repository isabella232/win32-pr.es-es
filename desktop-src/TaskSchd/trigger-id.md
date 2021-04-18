---
title: Propiedad Trigger.Id
description: Para el scripting, obtiene o establece el identificador del desencadenador.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Propiedad ID Programador de tareas
- Propiedad ID Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533945"
---
# <a name="triggerid-property"></a>Propiedad Trigger.Id

Para el scripting, obtiene o establece el identificador del desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador del desencadenador. El Programador de tareas usa este identificador para el registro.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, el identificador del desencadenador se especifica en el atributo ID de los elementos de desencadenador individuales (por ejemplo, el atributo ID del elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) del esquema programador de tareas.

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

 

 





