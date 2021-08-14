---
description: Las variables de condición son primitivas de sincronización que permiten a los subprocesos esperar hasta que se produce una condición determinada. Las variables de condición son objetos en modo de usuario que no se pueden compartir entre procesos.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variables de condición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d7ee98b4f5c5a65e633f7d1647b6c624840f9740efb639959c1500bec591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886365"
---
# <a name="condition-variables"></a>Variables de condición

Las variables de condición son primitivas de sincronización que permiten a los subprocesos esperar hasta que se produce una condición determinada. Las variables de condición son objetos en modo de usuario que no se pueden compartir entre procesos.

Las variables de condición permiten que los subprocesos liberen un bloqueo de forma atómica y entren en estado de espera. Se pueden usar con secciones críticas o bloqueos de lector/escritor (SRW). Las variables de condición admiten operaciones que "reactivan uno" o "reactivan todos" subprocesos en espera. Una vez que un subproceso se ha resarrodado, vuelve a adquirir el bloqueo que liberó cuando el subproceso entró en estado de bloqueo.

Tenga en cuenta que el autor de la llamada debe asignar una estructura **\_ CONDITION VARIABLE** e inicializarlo llamando a [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (para inicializar la estructura dinámicamente) o asignando la constante **CONDITION VARIABLE \_ \_ INIT** a la variable structure (para inicializar la estructura estáticamente).

**Windows Server 2003 y Windows XP:** No se admiten variables de condición.

Las siguientes son las funciones de variable de condición.



| Función de variable de condición                                        | Descripción                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Inicializa una variable de condición.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Se suspensión en la variable de condición especificada y libera la sección crítica especificada como una operación atómica. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Se bloquea en la variable de condición especificada y libera el bloqueo SRW especificado como una operación atómica.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Reactiva todos los subprocesos que esperan en la variable de condición especificada.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Reactiva un único subproceso que espera en la variable de condición especificada.                                             |



 

El pseudocódigo siguiente muestra el patrón de uso típico de las variables de condición.

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

Por ejemplo, en una implementación de un bloqueo lector/escritor, la función comprobaría que la solicitud de bloqueo actual `TestPredicate` es compatible con los propietarios existentes. Si es así, adquiera el bloqueo; de lo contrario, suspensión. Para obtener un ejemplo más detallado, vea [Usar variables de condición](using-condition-variables.md).

Las variables de condición están sujetas a reactivaciones falsos (aquellas que no están asociadas a una reactivación explícita) y reactivaciones robadas (otro subproceso se administra para ejecutarse antes que el subproceso desaprobado). Por lo tanto, debe volver a comprobar un predicado (normalmente en un **bucle while)** después de que se devuelva una operación de suspensión.

Puede reactivar otros subprocesos [**mediante WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) dentro o fuera del bloqueo asociado a la variable de condición. Normalmente es mejor liberar el bloqueo antes de activar otros subprocesos para reducir el número de modificadores de contexto.

A menudo resulta conveniente usar más de una variable de condición con el mismo bloqueo. Por ejemplo, una implementación de un bloqueo de lector/escritor podría usar una sola sección crítica, pero variables de condición independientes para lectores y escritores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar variables de condición](using-condition-variables.md)
</dt> </dl>

 

 
