---
description: Las siguientes funciones se usan con el control de errores.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Funciones de control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912765"
---
# <a name="error-handling-functions"></a>Funciones de control de errores

Las siguientes funciones se usan con el control de errores.



| Función                                                 | Descripción                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Señal sonora**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Genera tonos simples en el altavoz.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Captura un seguimiento de la pila de nuevo recorrindo la pila y registrando la información de cada fotograma.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Muestra un cuadro de mensaje y finaliza la aplicación cuando se cierra el cuadro de mensaje.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Parpadea la ventana especificada una vez.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Parpadea la ventana especificada.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Da formato a una cadena de mensaje.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Recupera el modo de error para el proceso actual.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Recupera el valor de código del último error del subproceso que realiza la llamada.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Recupera el modo de error para el subproceso que realiza la llamada.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Reproduce un sonido de forma de onda.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Busca en las tablas de funciones activas una entrada que se corresponda con el valor de PC especificado.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Recupera el código de error del sistema que corresponde al código de error NT especificado.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Recupera la dirección base de la imagen que contiene el valor de PC especificado.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Inicia un desenredo de fotogramas de llamada de procedimiento.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Inicia un desenredo de fotogramas de llamada de procedimiento.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Inicia un desenredo de fotogramas de llamada de procedimiento.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Recupera el contexto de invocación de la función que precede al contexto de función especificado.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Controla si el sistema controlará los tipos especificados de errores graves o si el proceso los controlará.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Establece el código del último error para el subproceso que realiza la llamada.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Establece el código del último error para el subproceso que realiza la llamada.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Controla si el sistema controlará los tipos especificados de errores graves o si el subproceso que realiza la llamada los controlará. |



 

 

 
