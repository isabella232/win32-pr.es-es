---
description: Hay dos ingredientes a la hora de determinar el comportamiento de la suplantación de la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad de los servidores de enmascarar su propia identidad al realizar llamadas en los clientes.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Cloaking (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807213"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="7113b-103">Cloaking (servicios de componentes)</span><span class="sxs-lookup"><span data-stu-id="7113b-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="7113b-104">Hay dos ingredientes a la hora de determinar el comportamiento de la suplantación: la autoridad que el cliente concede explícitamente al servidor a través de un nivel de suplantación y la capacidad del servidor de enmascarar su propia identidad al realizar llamadas en el nombre del cliente.</span><span class="sxs-lookup"><span data-stu-id="7113b-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="7113b-105">Esta última funcionalidad se conoce como *Cloaking*.</span><span class="sxs-lookup"><span data-stu-id="7113b-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="7113b-106">La ocultación tiene que hacer con la identidad de seguridad en la que el servidor realiza llamadas.</span><span class="sxs-lookup"><span data-stu-id="7113b-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="7113b-107">Cuando el servidor suplanta al cliente, tiene acceso directo a las credenciales de seguridad del cliente.</span><span class="sxs-lookup"><span data-stu-id="7113b-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="7113b-108">En un sentido muy local, el subproceso de servidor toma la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="7113b-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="7113b-109">Pero cuando el servidor realiza llamadas fuera de su proceso, la identidad del cliente no se proyectará necesariamente como la identidad en la que se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7113b-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="7113b-110">Cuando está habilitada la ocultación, las llamadas realizadas por el servidor que suplanta al cliente pueden realizarse en la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="7113b-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="7113b-111">Cuando se deshabilita la ocultación, las llamadas realizadas por el servidor se realizarán en la identidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="7113b-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="7113b-112">Además, hay dos formas de Cloaking, ocultación *estática* y *ocultación dinámica*, que se puede describir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7113b-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="7113b-113">Suplantación con Cloaking estático.</span><span class="sxs-lookup"><span data-stu-id="7113b-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="7113b-114">La identidad del cliente original (realizada como el token de subproceso de servidor) se puede presentar una vez a un servidor de nivel inferior en una llamada mediante [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), estableciendo la identidad del cliente original una vez en el proxy y ese token de subproceso se usará en las llamadas de método posteriores.</span><span class="sxs-lookup"><span data-stu-id="7113b-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="7113b-115">Suplantación con Cloaking dinámico.</span><span class="sxs-lookup"><span data-stu-id="7113b-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="7113b-116">La identidad del cliente original se detecta como el token del subproceso del servidor en cada llamada al método en el servidor que sigue en la cadena.</span><span class="sxs-lookup"><span data-stu-id="7113b-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="7113b-117">En efecto, la identidad que se presenta se puede determinar de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="7113b-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="7113b-118">La sobrecarga necesaria para ello puede ser considerablemente más costosa.</span><span class="sxs-lookup"><span data-stu-id="7113b-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="7113b-119">En el caso de las aplicaciones COM+, la configuración predeterminada es para la funcionalidad de ocultación dinámica.</span><span class="sxs-lookup"><span data-stu-id="7113b-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="7113b-120">Esto se puede cambiar mediante programación y administrativamente.</span><span class="sxs-lookup"><span data-stu-id="7113b-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="7113b-121">Aunque el Cloaking dinámico puede suponer una sobrecarga de rendimiento, proporciona la flexibilidad que normalmente requiere la realización de las circunstancias que requieren el uso de la suplantación en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="7113b-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="7113b-122">Para obtener más información acerca de la ocultación y descripciones precisas de posibles comportamientos, vea [cloakinging](/windows/desktop/com/cloaking) en la documentación de com.</span><span class="sxs-lookup"><span data-stu-id="7113b-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7113b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7113b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7113b-124">Suplantación y delegación de cliente</span><span class="sxs-lookup"><span data-stu-id="7113b-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="7113b-125">Requisitos del cliente para la suplantación</span><span class="sxs-lookup"><span data-stu-id="7113b-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="7113b-126">Requisitos del servidor para la suplantación</span><span class="sxs-lookup"><span data-stu-id="7113b-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
