---
description: En el ejemplo siguiente se asocia una función de llamada a procedimiento asincrónico (APC), también conocida como rutina de finalización, con un temporizador que se puede esperar cuando se establece el temporizador.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Usar temporizadores que se pueden esperar con una llamada a procedimiento asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661155"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Usar temporizadores que se pueden esperar con una llamada a procedimiento asincrónico

En el ejemplo siguiente se asocia una función [de](asynchronous-procedure-calls.md) llamada a procedimiento asincrónico (APC), también conocida como rutina de finalización, [con](waitable-timer-objects.md) un temporizador que se puede esperar cuando se establece el temporizador. La dirección de la rutina de finalización es el cuarto parámetro de la [**función SetWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) El quinto parámetro es un puntero void que puede usar para pasar argumentos a la rutina de finalización.

El mismo subproceso que llamó a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)ejecutará la rutina de finalización. Este subproceso debe estar en un estado de alerta para ejecutar la rutina de finalización. Para ello, llama a la [**función SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) que es una función que se puede alertar.

Cada subproceso tiene una cola de APC. Si hay una entrada en la cola de APC del subproceso en el momento en que se llama a una de las funciones que se pueden alertar, el subproceso no se pone en modo de suspensión. En su lugar, la entrada se quita de la cola de APC y se llama a la rutina de finalización.

Si no existe ninguna entrada en la cola de APC, el subproceso se suspende hasta que se cumple la espera. La espera se puede satisfacer agregando una entrada a la cola de APC, un tiempo de espera o un identificador que se señala. Si una entrada de la cola de APC satisface la espera, el subproceso se despeda y se llama a la rutina de finalización. En este caso, el valor devuelto de la función es **WAIT \_ IO \_ COMPLETION.**

Después de ejecutar la rutina de finalización, el sistema comprueba si hay otra entrada en la cola de APC que se va a procesar. Una función que admite alertas solo devolverá una vez procesadas todas las entradas de APC. Por lo tanto, si las entradas se agregan a la cola de APC más rápido de lo que se pueden procesar, es posible que nunca se devuelva una llamada a una función que puede alertar. Esto es especialmente posible con los temporizadores que se pueden esperar, si el período es más corto que la cantidad de tiempo necesaria para ejecutar la rutina de finalización.

Cuando se usa un temporizador que se puede esperar con un APC, el subproceso que establece el temporizador no debe esperar en el identificador del temporizador. Al hacerlo, haría que el subproceso se reactivase como resultado de que el temporizador se señalizase en lugar de como resultado de una entrada que se agrega a la cola de APC. Como resultado, el subproceso ya no está en estado de alerta y no se llama a la rutina de finalización. En el código siguiente, la llamada a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) llama al subproceso cuando se agrega una entrada a la cola de APC del subproceso después de establecer el temporizador en el estado señalado.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar objetos de temporizador que se pueden esperar](using-waitable-timer-objects.md)
</dt> </dl>

 

 
