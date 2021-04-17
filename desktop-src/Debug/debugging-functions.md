---
description: Las siguientes funciones se usan con la depuración.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Funciones de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659307"
---
# <a name="debugging-functions"></a>Funciones de depuración

Las siguientes funciones se usan con la depuración.



| Función                                                           | Descripción                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Determina si se está depurando el proceso especificado.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Permite a un depurador continuar un subproceso que anteriormente ha comunicado un evento de depuración. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Permite a un depurador asociarse a un proceso activo y depurarlo.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Detiene el depurador para depurar el proceso especificado.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Hace que se produzca una excepción de punto de interrupción en el proceso actual.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Hace que se produzca una excepción de punto de interrupción en el proceso especificado.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Establece la acción que se va a realizar cuando salga el subproceso que realiza la llamada.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Transfiere el control de ejecución al depurador.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Vacía la memoria caché de instrucciones para el proceso especificado.                            |
| [**GetThreadContext (**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Recupera el contexto del subproceso especificado.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Recupera una entrada de la tabla de descriptores para el selector y el subproceso especificados.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Determina si un depurador en modo de usuario está depurando el proceso de llamada.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Envía una cadena al depurador para su presentación.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Lee datos de un área de memoria en un proceso especificado.                           |
| [**SetThreadContext (**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Establece el contexto para el subproceso especificado.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Espera a que se produzca un evento de depuración en un proceso que se está depurando.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Recupera el contexto del subproceso WOW64 especificado.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Recupera una entrada de la tabla de descriptores para el selector y el subproceso WOW64 especificados.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Establece el contexto del subproceso WOW64 especificado.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Escribe datos en un área de memoria de un proceso especificado.                            |



 

 

 
