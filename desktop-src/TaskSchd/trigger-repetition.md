---
title: Propiedad Trigger.Repetition
description: Para el scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Propiedad De repetición Programador de tareas
- Propiedad De repetición Programador de tareas , Desencadenador de objeto
- Desencadenador de objetos Programador de tareas , propiedad De repetición
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
ms.openlocfilehash: 46e14b8dc23b329d9646647fdcc1c5bcb3166c5bf885886a5308c329e186dc51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002113"
---
# <a name="triggerrepetition-property"></a>Propiedad Trigger.Repetition

Para el scripting, obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**RepetitionPattern que**](repetitionpattern.md) define la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.

## <a name="remarks"></a>Comentarios

Al leer o escribir su propio XML para una tarea, el patrón de repetición de un desencadenador se especifica en el elemento [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) del esquema Programador de tareas datos.

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
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





