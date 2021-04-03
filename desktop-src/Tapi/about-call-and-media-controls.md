---
description: Los controles de llamada y multimedia de TAPI 3 son un conjunto genérico de objetos COM, interfaces y métodos para realizar llamadas entre dos o más máquinas.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Acerca de los controles de llamada y multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914182"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="2bd4a-103">Acerca de los controles de llamada y multimedia</span><span class="sxs-lookup"><span data-stu-id="2bd4a-103">About Call And Media Controls</span></span>

<span data-ttu-id="2bd4a-104">Los controles de llamada y multimedia de TAPI 3 son un conjunto genérico de objetos COM, interfaces y métodos para realizar llamadas entre dos o más máquinas.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="2bd4a-105">En el contexto de TAPI 3, la *llamada* a hace referencia no solo a la transmisión de voz a través de la red telefónica conmutada (RTC), sino a cualquier mecanismo medio y de transporte para el que existan proveedores de servicios: por ejemplo, una conferencia de multidifusión multimedia que se ejecute en una intranet corporativa.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="2bd4a-106">Los cinco objetos principales de la arquitectura de control multimedia y de llamadas TAPI 3 son [TAPI](tapi-object.md), [Dirección](address-object.md), [terminal](terminal-object.md), [llamada](call-object.md)y [CallHub](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="2bd4a-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="2bd4a-107">Además, se ha realizado el aprovisionamiento de [interfaces específicas del proveedor](provider-specific-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="2bd4a-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="2bd4a-108">En el diagrama siguiente se muestra cómo interactúan estos objetos.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-108">The following diagram illustrates how these objects interact.</span></span>

![interacciones entre los objetos de llamada y control multimedia de TAPI 3,0](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="2bd4a-110">Características</span><span class="sxs-lookup"><span data-stu-id="2bd4a-110">Features</span></span>

-   <span data-ttu-id="2bd4a-111">Abstrae la funcionalidad de llamada y multimedia para permitir que protocolos de comunicación diferentes y aparentemente incompatibles expongan una interfaz común a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="2bd4a-112">Basado en el modelo de objetos componentes (COM) para que las aplicaciones se puedan escribir prácticamente en cualquier lenguaje.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="2bd4a-113">Si necesita información adicional sobre COM, consulte el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="2bd4a-114">Control de llamadas proporcionado por los proveedores de servicios de telefonía (profesionales), que implementan mecanismos específicos del transporte.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="2bd4a-115">Control multimedia proporcionado por los proveedores de servicios multimedia (MSP).</span><span class="sxs-lookup"><span data-stu-id="2bd4a-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="2bd4a-116">Los MSP actuales usan DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="2bd4a-117">DirectShow es un sistema modular de componentes conectables denominado filtros, organizados en una configuración denominada gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="2bd4a-118">El administrador de gráficos de filtros supervisa la conexión de estos filtros y controla el flujo de datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="2bd4a-119">Si necesita información adicional sobre DirectShow, consulte el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="2bd4a-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



