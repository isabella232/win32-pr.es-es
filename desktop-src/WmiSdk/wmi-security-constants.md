---
description: WMI comprueba los derechos de acceso de las aplicaciones y los scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de seguridad de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278971"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="302e1-103">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="302e1-103">WMI Security Constants</span></span>

<span data-ttu-id="302e1-104">WMI comprueba los derechos de acceso de las aplicaciones y los scripts para objetos como los espacios de nombres WMI, la impresora, los servicios, las aplicaciones DCOM, los archivos, los recursos compartidos y otros objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="302e1-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="302e1-105">El acceso a estos objetos protegibles se controla mediante entradas de control de acceso (ACE).</span><span class="sxs-lookup"><span data-stu-id="302e1-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="302e1-106">Cada ACE contiene listas que designan qué grupos o usuarios tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="302e1-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="302e1-107">Para obtener más información sobre la seguridad y las listas de control de acceso (ACL, DACL o SACL), consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="302e1-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="302e1-108">Muchos métodos de proveedor de WMI que afectan a los objetos protegibles requieren que el administrador habilite determinados privilegios.</span><span class="sxs-lookup"><span data-stu-id="302e1-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="302e1-109">La versión del privilegio que use depende del lenguaje de programación, como se muestra en [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="302e1-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="302e1-110">Las constantes de seguridad se definen en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="302e1-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="302e1-111">**Constantes de seguridad de eventos**</span><span class="sxs-lookup"><span data-stu-id="302e1-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="302e1-112">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="302e1-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="302e1-113">**Constantes de derechos de acceso de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="302e1-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="302e1-114">**Constantes de marca ACE de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="302e1-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="302e1-115">**Constantes de tipo ACE de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="302e1-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="302e1-116">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="302e1-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
