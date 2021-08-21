---
description: El depurador usa la función WaitForDebugEvent al principio de su bucle main.
ms.assetid: 5a45854e-2711-49d5-982b-6b85248ec632
title: Escribir el bucle main del depurador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6695488e6391fa83a7d8aea999487beaae30360786872e3c345d52c201494cc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103895"
---
# <a name="writing-the-debuggers-main-loop"></a>Escribir el bucle main del depurador

El depurador usa la [**función WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) al principio de su bucle main. Esta función bloquea el depurador hasta que se produce un evento de depuración. Cuando se produce el evento de depuración, el sistema suspende todos los subprocesos del proceso que se está depurando y notifica al depurador del evento.

El depurador puede interactuar con el usuario o manipular el estado del proceso que se está depurando mediante las funciones [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext), [**GetThreadSelectorEntry,**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry) [**ReadProcessMemory,**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) [**y WriteProcessMemory.**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) **GetThreadSelectorEntry devuelve** la entrada de tabla de descriptores para un selector y subproceso especificados. Los depuradores usan la entrada de la tabla de descriptores para convertir una dirección relativa al segmento en una dirección virtual lineal. Las **funciones ReadProcessMemory** **y WriteProcessMemory** requieren direcciones virtuales lineales.

Los depuradores leen con frecuencia la memoria del proceso que se está depurando y escriben la memoria que contiene instrucciones en la memoria caché de instrucciones. Una vez escritas las instrucciones, el depurador llama a la función [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) para ejecutar las instrucciones almacenadas en caché.

El depurador usa la [**función ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) al final de su bucle principal. Esta función permite que el proceso que se está depurando continúe ejecutándose.

En el ejemplo siguiente se [**usan las funciones WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) y [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) para ilustrar cómo se podría organizar un depurador simple.


```C++
#include <windows.h>

DWORD OnCreateThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnCreateProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnLoadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnUnloadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnOutputDebugStringEvent(const LPDEBUG_EVENT);
DWORD OnRipEvent(const LPDEBUG_EVENT);

void EnterDebugLoop(const LPDEBUG_EVENT DebugEv)
{
   DWORD dwContinueStatus = DBG_CONTINUE; // exception continuation 
 
   for(;;) 
   { 
   // Wait for a debugging event to occur. The second parameter indicates
   // that the function does not return until a debugging event occurs. 
 
      WaitForDebugEvent(DebugEv, INFINITE); 

   // Process the debugging event code. 
 
      switch (DebugEv->dwDebugEventCode) 
      { 
         case EXCEPTION_DEBUG_EVENT: 
         // Process the exception code. When handling 
         // exceptions, remember to set the continuation 
         // status parameter (dwContinueStatus). This value 
         // is used by the ContinueDebugEvent function. 
 
            switch(DebugEv->u.Exception.ExceptionRecord.ExceptionCode)
            { 
               case EXCEPTION_ACCESS_VIOLATION: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_BREAKPOINT: 
               // First chance: Display the current 
               // instruction and register values. 
                  break;
 
               case EXCEPTION_DATATYPE_MISALIGNMENT: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_SINGLE_STEP: 
               // First chance: Update the display of the 
               // current instruction and register values. 
                  break;
 
               case DBG_CONTROL_C: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               default:
               // Handle other exceptions. 
                  break;
            } 

            break;
 
         case CREATE_THREAD_DEBUG_EVENT: 
         // As needed, examine or change the thread's registers 
         // with the GetThreadContext and SetThreadContext functions; 
         // and suspend and resume thread execution with the 
         // SuspendThread and ResumeThread functions. 

            dwContinueStatus = OnCreateThreadDebugEvent(DebugEv);
            break;

         case CREATE_PROCESS_DEBUG_EVENT: 
         // As needed, examine or change the registers of the
         // process's initial thread with the GetThreadContext and
         // SetThreadContext functions; read from and write to the
         // process's virtual memory with the ReadProcessMemory and
         // WriteProcessMemory functions; and suspend and resume
         // thread execution with the SuspendThread and ResumeThread
         // functions. Be sure to close the handle to the process image
         // file with CloseHandle.

            dwContinueStatus = OnCreateProcessDebugEvent(DebugEv);
            break;
 
         case EXIT_THREAD_DEBUG_EVENT: 
         // Display the thread's exit code. 

            dwContinueStatus = OnExitThreadDebugEvent(DebugEv);
            break;
 
         case EXIT_PROCESS_DEBUG_EVENT: 
         // Display the process's exit code. 

            dwContinueStatus = OnExitProcessDebugEvent(DebugEv);
            break;
 
         case LOAD_DLL_DEBUG_EVENT: 
         // Read the debugging information included in the newly 
         // loaded DLL. Be sure to close the handle to the loaded DLL 
         // with CloseHandle.

            dwContinueStatus = OnLoadDllDebugEvent(DebugEv);
            break;
 
         case UNLOAD_DLL_DEBUG_EVENT: 
         // Display a message that the DLL has been unloaded. 

            dwContinueStatus = OnUnloadDllDebugEvent(DebugEv);
            break;
 
         case OUTPUT_DEBUG_STRING_EVENT: 
         // Display the output debugging string. 

            dwContinueStatus = OnOutputDebugStringEvent(DebugEv);
            break;

         case RIP_EVENT:
            dwContinueStatus = OnRipEvent(DebugEv);
            break;
      } 
 
   // Resume executing the thread that reported the debugging event. 
 
   ContinueDebugEvent(DebugEv->dwProcessId, 
                      DebugEv->dwThreadId, 
                      dwContinueStatus);
   }
}
```



 

 
