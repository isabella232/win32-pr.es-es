---
title: Servicios críticos del sistema
description: El administrador de reinicio no puede detener y reiniciar los servicios críticos del sistema sin necesidad de reiniciar el sistema. Las actualizaciones de cualquier archivo o recurso en uso por uno de estos servicios requieren un reinicio del sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076415"
---
# <a name="critical-system-services"></a><span data-ttu-id="abc6c-104">Servicios críticos del sistema</span><span class="sxs-lookup"><span data-stu-id="abc6c-104">Critical System Services</span></span>

<span data-ttu-id="abc6c-105">El administrador de reinicio no puede detener y reiniciar los servicios críticos del sistema sin necesidad de reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="abc6c-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="abc6c-106">Las actualizaciones de cualquier archivo o recurso en uso por uno de estos servicios requieren un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="abc6c-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="abc6c-107">**Para determinar si un proceso es un servicio de sistema crítico.**</span><span class="sxs-lookup"><span data-stu-id="abc6c-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="abc6c-108">Registre el proceso mediante la función [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .</span><span class="sxs-lookup"><span data-stu-id="abc6c-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="abc6c-109">Llame a la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener la estructura de [**información del \_ proceso \_ de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .</span><span class="sxs-lookup"><span data-stu-id="abc6c-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="abc6c-110">El miembro **ApplicationType** de la estructura [**de \_ \_ información de proceso de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) devuelta contiene un valor de enumeración de [**\_ \_ tipo de aplicación de RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="abc6c-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="abc6c-111">Este valor se establece en **RmCriticial** para un proceso crítico del sistema.</span><span class="sxs-lookup"><span data-stu-id="abc6c-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="abc6c-112">Los servicios críticos del sistema incluyen smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, sistema, svchost.exe con RPCSS y svchost.exe con DCOM/PnP.</span><span class="sxs-lookup"><span data-stu-id="abc6c-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




