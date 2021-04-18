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
# <a name="condition-variables"></a><span data-ttu-id="7affe-104">Variables de condición</span><span class="sxs-lookup"><span data-stu-id="7affe-104">Condition Variables</span></span>

<span data-ttu-id="7affe-105">Las variables de condición son primitivas de sincronización que permiten a los subprocesos esperar hasta que se produce una condición determinada.</span><span class="sxs-lookup"><span data-stu-id="7affe-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="7affe-106">Las variables de condición son objetos de modo de usuario que no se pueden compartir entre los procesos.</span><span class="sxs-lookup"><span data-stu-id="7affe-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="7affe-107">Las variables de condición permiten a los subprocesos liberar un bloqueo de forma atómica y entrar en estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="7affe-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="7affe-108">Se pueden usar con secciones críticas o bloqueos finos de lector/escritor (SRW).</span><span class="sxs-lookup"><span data-stu-id="7affe-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="7affe-109">Las variables de condición admiten operaciones que "reactivan uno" o "reactivan todos" los subprocesos en espera.</span><span class="sxs-lookup"><span data-stu-id="7affe-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="7affe-110">Una vez que un subproceso se reactivarán, vuelve a adquirir el bloqueo que se libera cuando el subproceso entró en estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="7affe-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="7affe-111">Tenga en cuenta que el llamador debe asignar una estructura de **\_ variable de condición** e inicializarla mediante una llamada a [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (para inicializar la estructura dinámicamente) o asignar la **variable de condición Constant \_ \_ init** a la variable de estructura (para inicializar la estructura estáticamente).</span><span class="sxs-lookup"><span data-stu-id="7affe-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="7affe-112">**Windows Server 2003 y Windows XP:** No se admiten las variables de condición.</span><span class="sxs-lookup"><span data-stu-id="7affe-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="7affe-113">A continuación se muestran las funciones de variable de condición.</span><span class="sxs-lookup"><span data-stu-id="7affe-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="7affe-114">Función variable de condición</span><span class="sxs-lookup"><span data-stu-id="7affe-114">Condition variable function</span></span>                                        | <span data-ttu-id="7affe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7affe-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7affe-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="7affe-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="7affe-117">Inicializa una variable de condición.</span><span class="sxs-lookup"><span data-stu-id="7affe-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="7affe-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="7affe-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="7affe-119">Suspende en la variable de condición especificada y libera la sección crítica especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="7affe-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="7affe-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="7affe-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="7affe-121">Entra en suspensión en la variable de condición especificada y libera el bloqueo SRW especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="7affe-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="7affe-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="7affe-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="7affe-123">Activa todos los subprocesos que esperan en la variable de condición especificada.</span><span class="sxs-lookup"><span data-stu-id="7affe-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="7affe-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="7affe-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="7affe-125">Reactiva un único subproceso que espera en la variable de condición especificada.</span><span class="sxs-lookup"><span data-stu-id="7affe-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="7affe-126">En el siguiente pseudocódigo se muestra el patrón de uso típico de las variables de condición.</span><span class="sxs-lookup"><span data-stu-id="7affe-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

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

<span data-ttu-id="7affe-127">Por ejemplo, en una implementación de un bloqueo de lector/escritor, la `TestPredicate` función comprobará que la solicitud de bloqueo actual es compatible con los propietarios existentes.</span><span class="sxs-lookup"><span data-stu-id="7affe-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="7affe-128">Si es así, adquiera el bloqueo; en caso contrario, Sleep.</span><span class="sxs-lookup"><span data-stu-id="7affe-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="7affe-129">Para obtener un ejemplo más detallado, vea [using Condition variables](using-condition-variables.md).</span><span class="sxs-lookup"><span data-stu-id="7affe-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="7affe-130">Las variables de condición están sujetas a activaciones falsas (las que no están asociadas a una activación explícita) y a las activaciones robadas (otro subproceso administra para ejecutarse antes que el subproceso reactivarán).</span><span class="sxs-lookup"><span data-stu-id="7affe-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="7affe-131">Por lo tanto, debe volver a comprobar un predicado (normalmente en un bucle **While** ) después de que se devuelva una operación de suspensión.</span><span class="sxs-lookup"><span data-stu-id="7affe-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="7affe-132">Puede reactivar otros subprocesos mediante [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) dentro o fuera del bloqueo asociado a la variable de condición.</span><span class="sxs-lookup"><span data-stu-id="7affe-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="7affe-133">Normalmente es mejor liberar el bloqueo antes de activar otros subprocesos para reducir el número de cambios de contexto.</span><span class="sxs-lookup"><span data-stu-id="7affe-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="7affe-134">A menudo es conveniente usar más de una variable de condición con el mismo bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7affe-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="7affe-135">Por ejemplo, una implementación de un bloqueo de lector/escritor podría usar una sola sección crítica, pero variables de condición independientes para lectores y escritores.</span><span class="sxs-lookup"><span data-stu-id="7affe-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7affe-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7affe-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7affe-137">Usar variables de condición</span><span class="sxs-lookup"><span data-stu-id="7affe-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
