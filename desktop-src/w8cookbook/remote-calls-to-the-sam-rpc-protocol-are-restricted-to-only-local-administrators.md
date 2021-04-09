---
title: Las llamadas remotas al protocolo RPC de SAM están restringidas solo a los administradores locales
description: El protocolo RPC de SAM está restringido. Esto significa que solo los miembros del grupo de administradores locales pueden realizar llamadas remotas en métodos en este protocolo. Active Directory comportamiento del controlador de dominio no se ve afectado.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148861"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="a028f-105">Las llamadas remotas al protocolo RPC de SAM están restringidas solo a los administradores locales</span><span class="sxs-lookup"><span data-stu-id="a028f-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="a028f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a028f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a028f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a028f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a028f-108">El protocolo RPC de SAM está restringido.</span><span class="sxs-lookup"><span data-stu-id="a028f-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="a028f-109">Esto significa que solo los miembros del grupo de administradores locales pueden realizar llamadas remotas en métodos en este protocolo.</span><span class="sxs-lookup"><span data-stu-id="a028f-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="a028f-110">Active Directory comportamiento del controlador de dominio no se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="a028f-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="a028f-111">Mitigaciones</span><span class="sxs-lookup"><span data-stu-id="a028f-111">Mitigations</span></span>

<span data-ttu-id="a028f-112">Asegúrese de que los usuarios adecuados estén configurados como administradores en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a028f-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="a028f-113">La ACL utilizada para la comprobación de acceso se puede configurar mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a028f-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




