---
title: Trigger. repite (propiedad)
description: Para scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Programador de tareas de propiedad de repetición
- Propiedad repite Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad repite
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676679"
---
# <a name="triggerrepetition-property"></a>Trigger. repite (propiedad)

Para scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valor de propiedad

Un objeto [**RepetitionPattern**](repetitionpattern.md) que define la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, el patrón de repetición de un desencadenador se especifica en el elemento [**repite**](taskschedulerschema-repetition-triggerbasetype-element.md) del esquema de programador de tareas.

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
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





