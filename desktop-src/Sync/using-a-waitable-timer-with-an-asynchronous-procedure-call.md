---
description: En el ejemplo siguiente se asocia una función de llamada a procedimiento asincrónico (APC), también conocida como rutina de finalización, con un temporizador que se puede esperar cuando se establece el temporizador.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Usar temporizadores que esperan con una llamada a procedimiento asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667505"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a><span data-ttu-id="e82da-103">Usar temporizadores que esperan con una llamada a procedimiento asincrónica</span><span class="sxs-lookup"><span data-stu-id="e82da-103">Using Waitable Timers with an Asynchronous Procedure Call</span></span>

<span data-ttu-id="e82da-104">En el ejemplo siguiente se asocia una función de [llamada a procedimiento asincrónico](asynchronous-procedure-calls.md) (APC), también conocida como rutina de finalización, con un temporizador que se puede [esperar](waitable-timer-objects.md) cuando se establece el temporizador.</span><span class="sxs-lookup"><span data-stu-id="e82da-104">The following example associates an [asynchronous procedure call](asynchronous-procedure-calls.md) (APC) function, also known as a completion routine, with a [waitable timer](waitable-timer-objects.md) when the timer is set.</span></span> <span data-ttu-id="e82da-105">La dirección de la rutina de finalización es el cuarto parámetro de la función [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) .</span><span class="sxs-lookup"><span data-stu-id="e82da-105">The address of the completion routine is the fourth parameter to the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function.</span></span> <span data-ttu-id="e82da-106">El quinto parámetro es un puntero void que puede usar para pasar argumentos a la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-106">The fifth parameter is a void pointer that you can use to pass arguments to the completion routine.</span></span>

<span data-ttu-id="e82da-107">La rutina de finalización se ejecutará en el mismo subproceso que llamó a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span><span class="sxs-lookup"><span data-stu-id="e82da-107">The completion routine will be executed by the same thread that called [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span></span> <span data-ttu-id="e82da-108">Este subproceso debe estar en un estado de alerta para ejecutar la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-108">This thread must be in an alertable state to execute the completion routine.</span></span> <span data-ttu-id="e82da-109">Para ello, se llama a la función [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , que es una función de alerta.</span><span class="sxs-lookup"><span data-stu-id="e82da-109">It accomplishes this by calling the [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) function, which is an alertable function.</span></span>

<span data-ttu-id="e82da-110">Cada subproceso tiene una cola APC.</span><span class="sxs-lookup"><span data-stu-id="e82da-110">Each thread has an APC queue.</span></span> <span data-ttu-id="e82da-111">Si hay una entrada en la cola APC del subproceso en el momento en que se llama a una de las funciones de alerta, el subproceso no se pone en suspensión.</span><span class="sxs-lookup"><span data-stu-id="e82da-111">If there is an entry in the thread's APC queue at the time that one of the alertable functions is called, the thread is not put to sleep.</span></span> <span data-ttu-id="e82da-112">En su lugar, se quita la entrada de la cola APC y se llama a la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-112">Instead, the entry is removed from the APC queue and the completion routine is called.</span></span>

<span data-ttu-id="e82da-113">Si no existe ninguna entrada en la cola APC, el subproceso se suspende hasta que se cumple la espera.</span><span class="sxs-lookup"><span data-stu-id="e82da-113">If no entry exists in the APC queue, the thread is suspended until the wait is satisfied.</span></span> <span data-ttu-id="e82da-114">La espera se puede satisfacer mediante la adición de una entrada a la cola APC, un tiempo de espera o un controlador que se señaliza.</span><span class="sxs-lookup"><span data-stu-id="e82da-114">The wait can be satisfied by adding an entry to the APC queue, by a timeout, or by a handle becoming signaled.</span></span> <span data-ttu-id="e82da-115">Si una entrada satisface la espera en la cola APC, el subproceso se activa y se llama a la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-115">If the wait is satisfied by an entry in the APC queue, the thread is awakened and the completion routine is called.</span></span> <span data-ttu-id="e82da-116">En este caso, el valor devuelto de la función es la **\_ \_ finalización de la e/s de espera**.</span><span class="sxs-lookup"><span data-stu-id="e82da-116">In this case, the return value of the function is **WAIT\_IO\_COMPLETION**.</span></span>

<span data-ttu-id="e82da-117">Una vez ejecutada la rutina de finalización, el sistema comprueba si hay otra entrada en la cola APC para procesar.</span><span class="sxs-lookup"><span data-stu-id="e82da-117">After the completion routine is executed, the system checks for another entry in the APC queue to process.</span></span> <span data-ttu-id="e82da-118">Una función que se debe alertar solo devolverá una vez procesadas todas las entradas APC.</span><span class="sxs-lookup"><span data-stu-id="e82da-118">An alertable function will return only after all APC entries have been processed.</span></span> <span data-ttu-id="e82da-119">Por lo tanto, si las entradas se agregan a la cola APC más rápido de lo que se pueden procesar, es posible que una llamada a una función de alerta nunca devuelva.</span><span class="sxs-lookup"><span data-stu-id="e82da-119">Therefore, if entries are being added to the APC queue faster than they can be processed, it is possible that a call to an alertable function will never return.</span></span> <span data-ttu-id="e82da-120">Esto es especialmente posible con los temporizadores que esperan, si el período es más corto que la cantidad de tiempo necesario para ejecutar la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-120">This is especially possible with waitable timers, if the period is shorter than the amount of time required to execute the completion routine.</span></span>

<span data-ttu-id="e82da-121">Cuando se usa un temporizador que se puede esperar con una APC, el subproceso que establece el temporizador no debe esperar en el identificador del temporizador.</span><span class="sxs-lookup"><span data-stu-id="e82da-121">When you are using a waitable timer with an APC, the thread that sets the timer should not wait on the handle of the timer.</span></span> <span data-ttu-id="e82da-122">Al hacerlo, haría que el subproceso se reactivara como resultado de la señalización del temporizador en lugar de como resultado de la adición de una entrada a la cola APC.</span><span class="sxs-lookup"><span data-stu-id="e82da-122">By doing so, you would cause the thread to wake up as a result of the timer becoming signaled rather than as the result of an entry being added to the APC queue.</span></span> <span data-ttu-id="e82da-123">Como resultado, el subproceso ya no se encuentra en un estado de alerta y no se llama a la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="e82da-123">As a result, the thread is no longer in an alertable state and the completion routine is not called.</span></span> <span data-ttu-id="e82da-124">En el código siguiente, la llamada a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) pone al subproceso cuando se agrega una entrada a la cola APC del subproceso después de que el temporizador se haya establecido en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="e82da-124">In the following code, the call to [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) awakens the thread when an entry is added to the thread's APC queue after the timer is set to the signaled state.</span></span>


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="e82da-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e82da-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e82da-126">Usar objetos de temporizador de espera</span><span class="sxs-lookup"><span data-stu-id="e82da-126">Using Waitable Timer Objects</span></span>](using-waitable-timer-objects.md)
</dt> </dl>

 

 
