---
title: Modelo de ejecución
description: Modelo de ejecución
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de ejecución
- modelo de ejecución OpenGL
- OpenGL, modelo cliente/servidor
- modelo de cliente/servidor OpenGL
- OpenGL, transparente en red
- framebuffers, modelo de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994489"
---
# <a name="execution-model"></a><span data-ttu-id="2e05c-109">Modelo de ejecución</span><span class="sxs-lookup"><span data-stu-id="2e05c-109">Execution Model</span></span>

<span data-ttu-id="2e05c-110">El modelo para la interpretación de comandos OpenGL es cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="2e05c-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="2e05c-111">Código de la aplicación (el cliente) emite comandos, que se interpretan y procesan con OpenGL (el servidor).</span><span class="sxs-lookup"><span data-stu-id="2e05c-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="2e05c-112">El servidor puede funcionar o no en el mismo equipo que el cliente.</span><span class="sxs-lookup"><span data-stu-id="2e05c-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="2e05c-113">En este sentido, OpenGL es transparente en la red.</span><span class="sxs-lookup"><span data-stu-id="2e05c-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="2e05c-114">Un servidor puede mantener varios contextos de OpenGL, cada uno de los cuales es un estado de OpenGL encapsulado.</span><span class="sxs-lookup"><span data-stu-id="2e05c-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="2e05c-115">Un cliente puede conectarse a uno de estos contextos.</span><span class="sxs-lookup"><span data-stu-id="2e05c-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="2e05c-116">El protocolo de red necesario se puede implementar aumentando un protocolo ya existente (por ejemplo, el del sistema de ventanas X) o mediante un protocolo independiente.</span><span class="sxs-lookup"><span data-stu-id="2e05c-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="2e05c-117">No se proporciona ningún comando OpenGL para obtener datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2e05c-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="2e05c-118">En última instancia, el sistema de ventanas que asigna recursos fotogramas controla los efectos de los comandos OpenGL en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e05c-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="2e05c-119">El sistema de Windows:</span><span class="sxs-lookup"><span data-stu-id="2e05c-119">The window system:</span></span>

-   <span data-ttu-id="2e05c-120">Determina a qué partes de fotogramas OpenGL puede tener acceso en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="2e05c-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="2e05c-121">Se comunica con OpenGL cómo se estructuran esas partes.</span><span class="sxs-lookup"><span data-stu-id="2e05c-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="2e05c-122">Por lo tanto, no hay comandos OpenGL para configurar el fotogramas o inicializar OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2e05c-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="2e05c-123">La configuración del búfer de fotogramas se realiza fuera de OpenGL junto con el sistema de ventanas; La inicialización de OpenGL tiene lugar cuando el sistema de ventanas asigna una ventana para la representación de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2e05c-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




