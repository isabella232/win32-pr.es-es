---
description: Las siguientes funciones se usan con el control de errores.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Funciones de control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4cea391f05638310e17b9ef283e138204bc2cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152738"
---
# <a name="error-handling-functions"></a>Funciones de control de errores

Las siguientes funciones se usan con el control de errores.



| Función                                                 | Descripción                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Pitido**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Genera tonos simples en el altavoz.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Captura un seguimiento de la pila de retroceso recorriendo la pila y grabando la información de cada fotograma.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Muestra un cuadro de mensaje y finaliza la aplicación cuando el cuadro de mensaje está cerrado.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Parpadea la ventana especificada una vez.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Parpadea la ventana especificada.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Da formato a una cadena de mensaje.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Recupera el modo de error para el proceso actual.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Recupera el último valor del código de error del subproceso que realiza la llamada.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Recupera el modo de error para el subproceso que realiza la llamada.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Reproduce un sonido de onda.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Busca en las tablas de funciones activas una entrada que se corresponda con el valor de PC especificado.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Recupera el código de error del sistema correspondiente al código de error de NT especificado.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Recupera la dirección base de la imagen que contiene el valor de PC especificado.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Inicia un desenredado de los marcos de llamadas a procedimientos.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Inicia un desenredado de los marcos de llamadas a procedimientos.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Inicia un desenredado de los marcos de llamadas a procedimientos.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Recupera el contexto de invocación de la función que precede al contexto de función especificado.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Controla si el sistema controlará los tipos de errores graves especificados, o si el proceso los controlará.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Establece el último código de error para el subproceso que realiza la llamada.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Establece el último código de error para el subproceso que realiza la llamada.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Controla si el sistema controlará los tipos de errores graves especificados o si el subproceso que realiza la llamada los controlará. |



 

 

 
