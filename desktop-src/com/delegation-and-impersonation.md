---
title: Delegación y suplantación
description: En escenarios cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en el nombre de un cliente. La situación en la que se proporciona a un servidor la autoridad para actuar en nombre de un cliente se denomina delegación.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553612"
---
# <a name="delegation-and-impersonation"></a><span data-ttu-id="cff1e-104">Delegación y suplantación</span><span class="sxs-lookup"><span data-stu-id="cff1e-104">Delegation and Impersonation</span></span>

<span data-ttu-id="cff1e-105">En escenarios cliente/servidor, es habitual que un servidor llame a otro servidor para realizar alguna tarea en el nombre de un cliente.</span><span class="sxs-lookup"><span data-stu-id="cff1e-105">In client/server scenarios, it is common for one server to call another server to accomplish some task on a client's behalf.</span></span> <span data-ttu-id="cff1e-106">La situación en la que se proporciona a un servidor la autoridad para actuar en nombre de un cliente se denomina *delegación*.</span><span class="sxs-lookup"><span data-stu-id="cff1e-106">The situation where a server is given the authority to act on a client's behalf is called *delegation*.</span></span>

<span data-ttu-id="cff1e-107">Desde el punto de vista de la seguridad, surgen dos problemas relacionados con la delegación:</span><span class="sxs-lookup"><span data-stu-id="cff1e-107">From a security standpoint, two issues arise regarding delegation:</span></span>

-   <span data-ttu-id="cff1e-108">¿Qué debe permitir el servidor cuando actúa en nombre del cliente?</span><span class="sxs-lookup"><span data-stu-id="cff1e-108">What should the server be allowed to do when acting on the client's behalf?</span></span>
-   <span data-ttu-id="cff1e-109">¿Qué identidad presenta el servidor cuando llama a otros servidores en nombre de un cliente?</span><span class="sxs-lookup"><span data-stu-id="cff1e-109">What identity is presented by the server when it calls other servers on behalf of a client?</span></span>

<span data-ttu-id="cff1e-110">Para solucionar estos problemas, COM proporciona la siguiente funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="cff1e-110">To deal with these issues, COM provides the following functionality.</span></span> <span data-ttu-id="cff1e-111">El cliente puede establecer un *nivel de suplantación* que determina en qué medida el servidor podrá actuar como el cliente.</span><span class="sxs-lookup"><span data-stu-id="cff1e-111">The client can set an *impersonation level* that determines to what extent the server will be able to act as the client.</span></span> <span data-ttu-id="cff1e-112">Si el cliente concede suficiente autoridad para el servidor, el servidor puede *Suplantar* (fingir ser) el cliente.</span><span class="sxs-lookup"><span data-stu-id="cff1e-112">If the client grants enough authority to the server, the server can *impersonate* (pretend to be) the client.</span></span> <span data-ttu-id="cff1e-113">Al suplantar al cliente, al servidor se le concede acceso solo a los objetos o recursos que el cliente tiene permiso para usar.</span><span class="sxs-lookup"><span data-stu-id="cff1e-113">When impersonating the client, the server is given access to only those objects or resources that the client has permission to use.</span></span> <span data-ttu-id="cff1e-114">El servidor, que actúa como cliente, también puede habilitar la *ocultación* para enmascarar su propia identidad y proyectar la identidad del cliente en llamadas a otros componentes com.</span><span class="sxs-lookup"><span data-stu-id="cff1e-114">The server, acting as a client, can also enable *cloaking* to mask its own identity and project the client's identity in calls to other COM components.</span></span>

![Diagrama que muestra cómo el servidor que actúa como cliente puede habilitar la ocultación.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

<span data-ttu-id="cff1e-116">Considere el escenario que se muestra en la ilustración anterior, donde A y B son procesos en un equipo diferente de C. procesar una llamada B y B llama a C. el cliente A establece el nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="cff1e-116">Consider the scenario illustrated by the preceding figure, where A and B are processes on a different machine from C. Process A calls B, and B calls C. Client A sets the impersonation level.</span></span> <span data-ttu-id="cff1e-117">B establece la funcionalidad de ocultación.</span><span class="sxs-lookup"><span data-stu-id="cff1e-117">B sets the cloaking capability.</span></span> <span data-ttu-id="cff1e-118">Si un establece un nivel de suplantación que permite la suplantación, B puede suplantar A cuando se llama a C en nombre de.</span><span class="sxs-lookup"><span data-stu-id="cff1e-118">If A sets an impersonation level that permits impersonation, B can impersonate A when calling C on A's behalf.</span></span> <span data-ttu-id="cff1e-119">La identidad que se presenta al proceso C será la identidad o la identidad de B, en función de si la ocultación fue habilitada por B. Si está habilitada la ocultación, la identidad presentada al proceso C será la de. Si el Cloaking no está habilitado, la identidad de B se presentará en C.</span><span class="sxs-lookup"><span data-stu-id="cff1e-119">The identity that is presented to process C will be either A's identity or B's identity, depending on whether cloaking was enabled by B. If cloaking is enabled, the identity presented to process C will be that of A. If cloaking is not enabled, B's identity will be presented to C.</span></span>

<span data-ttu-id="cff1e-120">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="cff1e-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cff1e-121">Suplantación</span><span class="sxs-lookup"><span data-stu-id="cff1e-121">Impersonation</span></span>](impersonation.md)
-   [<span data-ttu-id="cff1e-122">Niveles de suplantación</span><span class="sxs-lookup"><span data-stu-id="cff1e-122">Impersonation Levels</span></span>](impersonation-levels.md)
-   [<span data-ttu-id="cff1e-123">Esconder</span><span class="sxs-lookup"><span data-stu-id="cff1e-123">Cloaking</span></span>](cloaking.md)

 

 




