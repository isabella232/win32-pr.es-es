---
description: En el siguiente ejemplo se bloquea la estación de trabajo mediante la función LockWorkStation. El sistema muestra el cuadro de diálogo bloquear estación de trabajo. El texto del cuadro de diálogo indica que la estación de trabajo está en uso y que el usuario la ha bloqueado.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Cómo bloquear la estación de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910330"
---
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="dc894-105">Cómo bloquear la estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="dc894-105">How to Lock the Workstation</span></span>

<span data-ttu-id="dc894-106">En el siguiente ejemplo se bloquea la estación de trabajo mediante la función [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) .</span><span class="sxs-lookup"><span data-stu-id="dc894-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="dc894-107">El sistema muestra el cuadro de diálogo **bloquear estación de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="dc894-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="dc894-108">El texto del cuadro de diálogo indica que la estación de trabajo está en uso y que el usuario la ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="dc894-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



<span data-ttu-id="dc894-109">Para determinar si la estación de trabajo está bloqueada, pruebe si la ventana está visible.</span><span class="sxs-lookup"><span data-stu-id="dc894-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="dc894-110">El usuario o un administrador pueden desbloquear la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="dc894-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="dc894-111">Para desbloquear el sistema, presione Ctrl + Alt + Supr e inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="dc894-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="dc894-112">Para recibir una notificación cuando el usuario inicie sesión, utilice la función [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) para registrarse y recibir los mensajes de [**cambio de \_ WTSSESSION \_ de WM**](../termserv/wm-wtssession-change.md) .</span><span class="sxs-lookup"><span data-stu-id="dc894-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="dc894-113">Cuando se reciba este mensaje, compruebe si el parámetro *wParam* es igual al bloqueo de la sesión de WTS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dc894-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
