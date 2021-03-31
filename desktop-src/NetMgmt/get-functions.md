---
title: Funciones Get
description: Las funciones de obtención de administración de red recuperan información sobre un dominio. También puede llamar a estas funciones para recuperar información acerca de las cuentas de usuario locales, globales, de estación de trabajo y de servidor.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532236"
---
# <a name="get-functions"></a><span data-ttu-id="e3ad9-104">Funciones Get</span><span class="sxs-lookup"><span data-stu-id="e3ad9-104">Get Functions</span></span>

<span data-ttu-id="e3ad9-105">Las funciones de obtención de administración de red recuperan información sobre un dominio.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="e3ad9-106">También puede llamar a estas funciones para recuperar información acerca de las cuentas de usuario locales, globales, de estación de trabajo y de servidor.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="e3ad9-107">A continuación se enumeran las funciones de obtención de administración de red.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="e3ad9-108">Función</span><span class="sxs-lookup"><span data-stu-id="e3ad9-108">Function</span></span>                                                               | <span data-ttu-id="e3ad9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ad9-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3ad9-110">**NetGetAnyDCName**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="e3ad9-111">Devuelve el nombre de cualquier controlador de dominio para un dominio que sea de confianza directa para un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="e3ad9-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="e3ad9-113">Devuelve el nombre del controlador de dominio principal (PDC) para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="e3ad9-114">**NetGetDisplayInformationIndex**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="e3ad9-115">Devuelve el índice de la primera entrada de información de visualización cuyo nombre comienza con una cadena especificada o que sigue alfabéticamente a la cadena.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="e3ad9-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="e3ad9-117">Devuelve la información de la cuenta de usuario, equipo o grupo global.</span><span class="sxs-lookup"><span data-stu-id="e3ad9-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="e3ad9-118">La información devuelta por la función [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) está disponible en los siguientes niveles:</span><span class="sxs-lookup"><span data-stu-id="e3ad9-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="e3ad9-119">**NET \_ Display \_ Group**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="e3ad9-120">**NET \_ Display \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="e3ad9-121">**NET \_ Display \_ User**</span><span class="sxs-lookup"><span data-stu-id="e3ad9-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




