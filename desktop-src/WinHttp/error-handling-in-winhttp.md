---
description: Control de errores en WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Control de errores en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706851"
---
# <a name="error-handling-in-winhttp"></a>Control de errores en WinHTTP

No todas las funciones de la API de WinHTTP notifican errores de la misma manera.

Algunas funciones, como [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), devuelven un valor **booleano** que indica un error cuando **es false**. Si se devuelve **false** , los llamadores interesados en el error deben llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si se llama a **GetLastError** cuando la función correctos (devuelve cualquier cosa pero **false**), el valor devuelto es imprevisible y puede cambiar entre versiones de Windows, Service Packs o incluso entre llamadas a la misma función.

Algunas funciones, como [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), devuelven un pseudo identificador de [HINTERNET](hinternet-handles-in-winhttp.md) . Estas funciones son exactamente iguales, salvo que el error se indica devolviendo **null**. Si se devuelve **null** , los llamadores interesados en el error deben llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si se llama a **GetLastError** cuando la función correctos (devuelve cualquier cosa pero **null**), el valor devuelto es imprevisible y puede cambiar entre versiones de Windows, Service Packs o incluso entre llamadas a la misma función.

Algunas funciones, como [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), devuelven un código de error **DWORD** y no es necesario llamar a otras funciones para obtener más información sobre el error. Para estas funciones, no se debe llamar a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) . Si se llama a **GetLastError** , independientemente de si la función se ha realizado correctamente o no, el valor devuelto es imprevisible y puede cambiar entre versiones de Windows, Service Pack o incluso entre llamadas a la misma función.

 

 
