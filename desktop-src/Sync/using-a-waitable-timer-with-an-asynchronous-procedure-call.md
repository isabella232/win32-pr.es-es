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
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Usar temporizadores que esperan con una llamada a procedimiento asincrónica

En el ejemplo siguiente se asocia una función de [llamada a procedimiento asincrónico](asynchronous-procedure-calls.md) (APC), también conocida como rutina de finalización, con un temporizador que se puede [esperar](waitable-timer-objects.md) cuando se establece el temporizador. La dirección de la rutina de finalización es el cuarto parámetro de la función [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) . El quinto parámetro es un puntero void que puede usar para pasar argumentos a la rutina de finalización.

La rutina de finalización se ejecutará en el mismo subproceso que llamó a [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Este subproceso debe estar en un estado de alerta para ejecutar la rutina de finalización. Para ello, se llama a la función [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , que es una función de alerta.

Cada subproceso tiene una cola APC. Si hay una entrada en la cola APC del subproceso en el momento en que se llama a una de las funciones de alerta, el subproceso no se pone en suspensión. En su lugar, se quita la entrada de la cola APC y se llama a la rutina de finalización.

Si no existe ninguna entrada en la cola APC, el subproceso se suspende hasta que se cumple la espera. La espera se puede satisfacer mediante la adición de una entrada a la cola APC, un tiempo de espera o un controlador que se señaliza. Si una entrada satisface la espera en la cola APC, el subproceso se activa y se llama a la rutina de finalización. En este caso, el valor devuelto de la función es la **\_ \_ finalización de la e/s de espera**.

Una vez ejecutada la rutina de finalización, el sistema comprueba si hay otra entrada en la cola APC para procesar. Una función que se debe alertar solo devolverá una vez procesadas todas las entradas APC. Por lo tanto, si las entradas se agregan a la cola APC más rápido de lo que se pueden procesar, es posible que una llamada a una función de alerta nunca devuelva. Esto es especialmente posible con los temporizadores que esperan, si el período es más corto que la cantidad de tiempo necesario para ejecutar la rutina de finalización.

Cuando se usa un temporizador que se puede esperar con una APC, el subproceso que establece el temporizador no debe esperar en el identificador del temporizador. Al hacerlo, haría que el subproceso se reactivara como resultado de la señalización del temporizador en lugar de como resultado de la adición de una entrada a la cola APC. Como resultado, el subproceso ya no se encuentra en un estado de alerta y no se llama a la rutina de finalización. En el código siguiente, la llamada a [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) pone al subproceso cuando se agrega una entrada a la cola APC del subproceso después de que el temporizador se haya establecido en el estado señalado.


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

[Usar objetos de temporizador de espera](using-waitable-timer-objects.md)
</dt> </dl>

 

 
