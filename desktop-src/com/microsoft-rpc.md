---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772787"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="e4b9e-103">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="e4b9e-103">Microsoft RPC</span></span>

<span data-ttu-id="e4b9e-104">Microsoft RPC es un modelo de programación en un entorno de computación distribuida.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="e4b9e-105">El objetivo de RPC es proporcionar una comunicación transparente para que el cliente parezca que se comunica directamente con el servidor.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="e4b9e-106">La implementación de RPC de Microsoft es compatible con el RPC del entorno de computación distribuida (DCE) de Open Software Foundation (OSF).</span><span class="sxs-lookup"><span data-stu-id="e4b9e-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="e4b9e-107">Puede configurar RPC para usar uno o más transportes, uno o más servicios de nombre y uno o varios servidores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="e4b9e-108">RPC administra las interfaces a esos proveedores.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="e4b9e-109">Dado que Microsoft RPC está diseñado para trabajar con varios proveedores, puede elegir los proveedores que mejor funcionan para la red.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="e4b9e-110">El transporte es responsable de la transmisión de los datos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="e4b9e-111">El servicio de nombres toma un nombre de objeto, como un moniker, y busca su ubicación en la red.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="e4b9e-112">El servidor de seguridad ofrece a las aplicaciones la opción de denegar el acceso a usuarios o grupos específicos.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="e4b9e-113">Vea [reglas de diseño de interfaz](interface-design-rules.md) para obtener información más detallada sobre la seguridad de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="e4b9e-114">Además de las bibliotecas en tiempo de ejecución de RPC, Microsoft RPC incluye el lenguaje de definición de interfaz (IDL) y su compilador.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="e4b9e-115">Aunque el archivo IDL es una parte estándar de RPC, Microsoft lo ha mejorado para ampliar su funcionalidad con el fin de admitir interfaces COM personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e4b9e-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="e4b9e-116">El compilador de Lenguaje de definición de interfaz de Microsoft (MIDL) utiliza el archivo IDL que describe la interfaz personalizada para generar varios archivos que se describen en [Building and registrating a proxy dll](building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="e4b9e-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4b9e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4b9e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b9e-118">Canal</span><span class="sxs-lookup"><span data-stu-id="e4b9e-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="e4b9e-119">Comunicación entre objetos</span><span class="sxs-lookup"><span data-stu-id="e4b9e-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="e4b9e-120">Detalles de serialización</span><span class="sxs-lookup"><span data-stu-id="e4b9e-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="e4b9e-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="e4b9e-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="e4b9e-122">Stub</span><span class="sxs-lookup"><span data-stu-id="e4b9e-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




