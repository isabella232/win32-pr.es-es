---
description: La siguiente definición de Winternl. h es la dirección de memoria estática del identificador de sesión de la consola de Terminal Services activa. Este identificador de sesión de consola activa no está definido en las versiones del sistema operativo Microsoft Windows anteriores a Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obtención del ID. de sesión de la consola activa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907164"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="f5646-104">Obtención del ID. de sesión de la consola activa</span><span class="sxs-lookup"><span data-stu-id="f5646-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="f5646-105">La siguiente definición de Winternl. h es la dirección de memoria estática del identificador de sesión de la consola de Terminal Services activa.</span><span class="sxs-lookup"><span data-stu-id="f5646-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="f5646-106">Este identificador de sesión de consola activa no está definido en las versiones del sistema operativo Microsoft Windows anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5646-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="f5646-107">Esta definición puede cambiar en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="f5646-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="f5646-108">Para asegurarse de que la aplicación se siga ejecutando correctamente en el futuro, la aplicación debe llamar a [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span><span class="sxs-lookup"><span data-stu-id="f5646-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
