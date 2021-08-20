---
description: Las siguientes funciones se usan con la depuración.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Funciones de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfafdf5a453d262e75c4ab87356cbe34cfbb8574b520d353de0e66057903087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162676"
---
# <a name="debugging-functions"></a>Funciones de depuración

Las siguientes funciones se usan con la depuración.



| Función                                                           | Descripción                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Determina si se está depurando el proceso especificado.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Permite que un depurador continúe con un subproceso que previamente informó de un evento de depuración. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Permite que un depurador se asocie a un proceso activo y lo depure.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Impide que el depurador depure el proceso especificado.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Hace que se produzca una excepción de punto de interrupción en el proceso actual.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Hace que se produzca una excepción de punto de interrupción en el proceso especificado.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Establece la acción que se va a realizar cuando se cierre el subproceso que realiza la llamada.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Transfiere el control de ejecución al depurador.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Vacía la memoria caché de instrucciones para el proceso especificado.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Recupera el contexto del subproceso especificado.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Recupera una entrada de tabla descriptor para el selector y subproceso especificados.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Determina si un depurador en modo de usuario depura el proceso de llamada.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Envía una cadena al depurador para mostrarla.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Lee datos de un área de memoria en un proceso especificado.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Establece el contexto del subproceso especificado.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Espera a que se produzca un evento de depuración en un proceso que se está depurando.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Recupera el contexto del subproceso WOW64 especificado.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Recupera una entrada de tabla descriptor para el selector y subproceso WOW64 especificados.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Establece el contexto del subproceso WOW64 especificado.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Escribe datos en un área de memoria en un proceso especificado.                            |



 

 

 
