---
title: Establecer la seguridad de las aplicaciones COM
description: Establecer la seguridad de las aplicaciones COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903911"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="beb33-103">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="beb33-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="beb33-104">Hay varias maneras de ayudar a controlar la seguridad de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="beb33-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="beb33-105">Puede cambiar la configuración de seguridad predeterminada de un equipo, que son utilizadas por todas las aplicaciones del equipo que no proporcionan sus propios valores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="beb33-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="beb33-106">Puede establecer la seguridad de un proceso determinado, ya sea mediante Dcomcnfg.exe o mediante una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="beb33-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="beb33-107">También puede controlar mediante programación la configuración de seguridad en el nivel de proxy de interfaz.</span><span class="sxs-lookup"><span data-stu-id="beb33-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="beb33-108">En los temas siguientes se proporcionan procedimientos que explican cómo establecer la seguridad:</span><span class="sxs-lookup"><span data-stu-id="beb33-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="beb33-109">Modificación de los valores predeterminados de seguridad de un equipo</span><span class="sxs-lookup"><span data-stu-id="beb33-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="beb33-110">Configuración de la seguridad de Process-Wide</span><span class="sxs-lookup"><span data-stu-id="beb33-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="beb33-111">Establecimiento de la seguridad en el nivel de proxy de interfaz</span><span class="sxs-lookup"><span data-stu-id="beb33-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="beb33-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="beb33-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb33-113">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="beb33-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




