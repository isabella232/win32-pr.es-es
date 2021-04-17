---
description: En el material siguiente se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de usuario final o de servidor. Esta información también es muy relevante para los programadores de proveedores de servicios.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Aplicaciones TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678357"
---
# <a name="tapi-applications"></a><span data-ttu-id="1c604-104">Aplicaciones TAPI</span><span class="sxs-lookup"><span data-stu-id="1c604-104">TAPI Applications</span></span>

<span data-ttu-id="1c604-105">En el material siguiente se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de usuario final o de servidor.</span><span class="sxs-lookup"><span data-stu-id="1c604-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="1c604-106">Esta información también es muy relevante para los programadores de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="1c604-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="1c604-107">La primera decisión que debe realizar un programador al usar TAPI es el nivel de servicio requerido.</span><span class="sxs-lookup"><span data-stu-id="1c604-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="1c604-108">Por ejemplo, si una aplicación requiere una selección de menú que puede marcar un número de teléfono, es probable que no se requiera una aplicación TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="1c604-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="1c604-109">La telefonía asistida puede habilitar esta opción de forma rápida y sencilla.</span><span class="sxs-lookup"><span data-stu-id="1c604-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="1c604-110">Consulte [niveles de servicio de TAPI](tapi-levels-of-service.md) para obtener más información acerca de la diferencia entre las aplicaciones TAPI completas y la telefonía asistida.</span><span class="sxs-lookup"><span data-stu-id="1c604-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="1c604-111">La segunda decisión importante es si se usa TAPI 2. x, la API basada en C o TAPI 3. x, que se basa en COM.</span><span class="sxs-lookup"><span data-stu-id="1c604-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="1c604-112">Consulte [TAPI 3. x frente a TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) para obtener una explicación de las consideraciones importantes a la hora de decidir cuál usar.</span><span class="sxs-lookup"><span data-stu-id="1c604-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="1c604-113">En el diagrama siguiente se ilustran los bloques de creación básicos de una aplicación TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="1c604-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="1c604-114">TAPI 2. x y TAPI 3. x se tratan en estas secciones.</span><span class="sxs-lookup"><span data-stu-id="1c604-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="1c604-115">En las secciones de información general de TAPI 2. x o TAPI 3. x se trata el material muy específico de uno.</span><span class="sxs-lookup"><span data-stu-id="1c604-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![bloques de creación de una aplicación TAPI](images/tapior3.png)

<span data-ttu-id="1c604-117">Los vínculos siguientes proporcionan contenido que corresponde a las cifras de la imagen anterior:</span><span class="sxs-lookup"><span data-stu-id="1c604-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="1c604-118">Figura</span><span class="sxs-lookup"><span data-stu-id="1c604-118">Figure</span></span> | <span data-ttu-id="1c604-119">Documentación</span><span class="sxs-lookup"><span data-stu-id="1c604-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1c604-120">1</span><span class="sxs-lookup"><span data-stu-id="1c604-120">1</span></span>      | [<span data-ttu-id="1c604-121">Inicialización de TAPI</span><span class="sxs-lookup"><span data-stu-id="1c604-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="1c604-122">2</span><span class="sxs-lookup"><span data-stu-id="1c604-122">2</span></span>      | [<span data-ttu-id="1c604-123">Control de sesión</span><span class="sxs-lookup"><span data-stu-id="1c604-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="1c604-124">3</span><span class="sxs-lookup"><span data-stu-id="1c604-124">3</span></span>      | [<span data-ttu-id="1c604-125">Control de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1c604-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="1c604-126">4</span><span class="sxs-lookup"><span data-stu-id="1c604-126">4</span></span>      | [<span data-ttu-id="1c604-127">Control multimedia</span><span class="sxs-lookup"><span data-stu-id="1c604-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="1c604-128">5</span><span class="sxs-lookup"><span data-stu-id="1c604-128">5</span></span>      | [<span data-ttu-id="1c604-129">Acerca de los controles de centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="1c604-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="1c604-130">6</span><span class="sxs-lookup"><span data-stu-id="1c604-130">6</span></span>      | [<span data-ttu-id="1c604-131">Conferencias de telefonía IP de encuentro</span><span class="sxs-lookup"><span data-stu-id="1c604-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="1c604-132">7</span><span class="sxs-lookup"><span data-stu-id="1c604-132">7</span></span>      | [<span data-ttu-id="1c604-133">Apagado de TAPI</span><span class="sxs-lookup"><span data-stu-id="1c604-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



