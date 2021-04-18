---
description: Las variables de condición son primitivas de sincronización que permiten a los subprocesos esperar hasta que se produce una condición determinada. Las variables de condición son objetos de modo de usuario que no se pueden compartir entre los procesos.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variables de condición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667981"
---
# <a name="condition-variables"></a>Variables de condición

Las variables de condición son primitivas de sincronización que permiten a los subprocesos esperar hasta que se produce una condición determinada. Las variables de condición son objetos de modo de usuario que no se pueden compartir entre los procesos.

Las variables de condición permiten a los subprocesos liberar un bloqueo de forma atómica y entrar en estado de inactividad. Se pueden usar con secciones críticas o bloqueos finos de lector/escritor (SRW). Las variables de condición admiten operaciones que "reactivan uno" o "reactivan todos" los subprocesos en espera. Una vez que un subproceso se reactivarán, vuelve a adquirir el bloqueo que se libera cuando el subproceso entró en estado de inactividad.

Tenga en cuenta que el llamador debe asignar una estructura de **\_ variable de condición** e inicializarla mediante una llamada a [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (para inicializar la estructura dinámicamente) o asignar la **variable de condición Constant \_ \_ init** a la variable de estructura (para inicializar la estructura estáticamente).

**Windows Server 2003 y Windows XP:** No se admiten las variables de condición.

A continuación se muestran las funciones de variable de condición.



| Función variable de condición                                        | Descripción                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Inicializa una variable de condición.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Suspende en la variable de condición especificada y libera la sección crítica especificada como una operación atómica. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Entra en suspensión en la variable de condición especificada y libera el bloqueo SRW especificado como una operación atómica.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Activa todos los subprocesos que esperan en la variable de condición especificada.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Reactiva un único subproceso que espera en la variable de condición especificada.                                             |



 

En el siguiente pseudocódigo se muestra el patrón de uso típico de las variables de condición.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Por ejemplo, en una implementación de un bloqueo de lector/escritor, la `TestPredicate` función comprobará que la solicitud de bloqueo actual es compatible con los propietarios existentes. Si es así, adquiera el bloqueo; en caso contrario, Sleep. Para obtener un ejemplo más detallado, vea [using Condition variables](using-condition-variables.md).

Las variables de condición están sujetas a activaciones falsas (las que no están asociadas a una activación explícita) y a las activaciones robadas (otro subproceso administra para ejecutarse antes que el subproceso reactivarán). Por lo tanto, debe volver a comprobar un predicado (normalmente en un bucle **While** ) después de que se devuelva una operación de suspensión.

Puede reactivar otros subprocesos mediante [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) dentro o fuera del bloqueo asociado a la variable de condición. Normalmente es mejor liberar el bloqueo antes de activar otros subprocesos para reducir el número de cambios de contexto.

A menudo es conveniente usar más de una variable de condición con el mismo bloqueo. Por ejemplo, una implementación de un bloqueo de lector/escritor podría usar una sola sección crítica, pero variables de condición independientes para lectores y escritores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar variables de condición](using-condition-variables.md)
</dt> </dl>

 

 
