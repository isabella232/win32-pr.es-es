---
description: Control de errores en WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Control de errores en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899195"
---
# <a name="error-handling-in-winhttp"></a>Control de errores en WinHTTP

No todas las funciones de api WinHTTP informan de errores de la misma manera.

Algunas funciones, como [**WinHttpSetTimeouts,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)devuelven un **valor BOOL** que indica un error cuando **es FALSE.** Si **se devuelve FALSE,** los autores de la llamada interesados en el error deben llamar [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si se llama a **GetLastError** cuando la función tiene éxito (devuelve cualquier cosa menos **FALSE),** el valor devuelto es impredecible y puede cambiar entre versiones de Windows, Service Packs o incluso entre llamadas a la misma función.

Algunas funciones, como [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)devuelven un pseudo identificador [HINTERNET.](hinternet-handles-in-winhttp.md) Estas funciones son exactamente iguales, salvo que el error se indica devolviendo **NULL.** Si **se devuelve NULL,** los autores de la llamada interesados en el error deben llamar [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si se llama a **GetLastError** cuando la función ha funcionado correctamente (devuelve algo menos **NULL),** el valor devuelto es imprevisible y puede cambiar entre versiones de Windows, Service Packs o incluso entre llamadas a la misma función.

Algunas funciones, como [**WinHttpGetProxyResult,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)devuelven un código de error **DWORD** y no es necesario llamar a ninguna otra función para obtener más información de error. Para estas funciones, no se debe llamar a [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Si se llama a **GetLastError,** independientemente del éxito o error de la función, el valor devuelto es imprevisible y puede cambiar entre versiones de Windows, Service Packs o incluso entre llamadas a la misma función.

 

 
