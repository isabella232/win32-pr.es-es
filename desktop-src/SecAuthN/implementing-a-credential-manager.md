---
description: Muestra las exportaciones de DLL que se deben implementar para crear un administrador de credenciales.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementación de un administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912481"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="ec86e-103">Implementación de un administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="ec86e-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="ec86e-104">Para crear un administrador de credenciales, debe crear un archivo DLL que exporte las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="ec86e-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="ec86e-105">**NPLogonNotify**</span><span class="sxs-lookup"><span data-stu-id="ec86e-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="ec86e-106">**NPPasswordChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="ec86e-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="ec86e-107">Para restaurar las notificaciones a las funciones [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para el inicio de sesión con tarjeta inteligente, cree una entrada del registro denominada **SmartCardLogonNotify** como **DWORD** y establézcala en 1:</span><span class="sxs-lookup"><span data-stu-id="ec86e-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="ec86e-108">**Windows Server 2003 y Windows XP:** La entrada del registro **SmartCardLogonNotify** no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="ec86e-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="ec86e-109">Además, los administradores de credenciales también deben admitir la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para WNNC \_ Start (no es necesario admitir otros índices para los administradores de credenciales).</span><span class="sxs-lookup"><span data-stu-id="ec86e-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="ec86e-110">Esto indica a MPR Cuándo se iniciará un administrador de credenciales.</span><span class="sxs-lookup"><span data-stu-id="ec86e-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="ec86e-111">Al llamar a **NPGetCaps** con el parámetro *NINDEX* establecido en WNNC \_ Start, el MPR obtiene el tiempo de espera antes de llamar a las funciones de punto de entrada de administración de credenciales del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ec86e-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="ec86e-112">Y si el MPR tiene esta información, puede reenviarla al administrador de credenciales y establecer el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="ec86e-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



