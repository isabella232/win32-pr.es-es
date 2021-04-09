---
description: El siguiente código limpia toda la memoria asociada al control de símbolos para el proceso especificado, mediante SymCleanup.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Finalización del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9147ed15c0dc03b76c822a38ccd7ac3c5d326454
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153104"
---
# <a name="terminating-the-symbol-handler"></a>Finalización del controlador de símbolos

El siguiente código limpia toda la memoria asociada al control de símbolos para el proceso especificado, mediante [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



