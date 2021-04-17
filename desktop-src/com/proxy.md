---
title: Proxy
description: Un proxy reside en el espacio de direcciones del proceso de llamada y actúa como suplente del objeto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105717315"
---
# <a name="proxy"></a><span data-ttu-id="f5edf-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="f5edf-103">Proxy</span></span>

<span data-ttu-id="f5edf-104">Un proxy reside en el espacio de direcciones del proceso de llamada y actúa como suplente del objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="f5edf-105">Desde la perspectiva del objeto que realiza la llamada, el proxy es el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="f5edf-106">Normalmente, el rol del proxy es empaquetar los parámetros de la interfaz para las llamadas a métodos en sus interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="f5edf-107">El proxy empaqueta los parámetros en un búfer de mensajes y pasa el búfer al canal, que controla el transporte entre los procesos.</span><span class="sxs-lookup"><span data-stu-id="f5edf-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="f5edf-108">El proxy se implementa como un objeto agregado o compuesto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="f5edf-109">Contiene un elemento de administrador proporcionado por el sistema denominado administrador de proxy y uno o varios componentes específicos de la interfaz denominados proxies de interfaz.</span><span class="sxs-lookup"><span data-stu-id="f5edf-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="f5edf-110">El número de proxies de interfaz es igual al número de interfaces de objeto que se han expuesto a ese cliente concreto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="f5edf-111">Para que el cliente cumpla con el modelo de objetos componentes, el proxy parece ser el objeto real.</span><span class="sxs-lookup"><span data-stu-id="f5edf-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="f5edf-112">Con el cálculo de referencias personalizado, el proxy se puede implementar de forma similar o se puede comunicar directamente con el objeto sin usar un código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f5edf-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="f5edf-113">Cada proxy de interfaz es un objeto de componente que implementa el código de serialización para una de las interfaces del objeto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="f5edf-114">El proxy representa el objeto para el que proporciona el código de serialización.</span><span class="sxs-lookup"><span data-stu-id="f5edf-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="f5edf-115">Cada proxy también implementa la interfaz [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) .</span><span class="sxs-lookup"><span data-stu-id="f5edf-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="f5edf-116">Aunque la interfaz de objeto representada por el proxy es pública, la implementación de **IRpcProxyBuffer** es privada y se usa internamente dentro del proxy.</span><span class="sxs-lookup"><span data-stu-id="f5edf-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="f5edf-117">El administrador de proxy realiza un seguimiento de los proxies de interfaz y también contiene la implementación pública de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control para el agregado.</span><span class="sxs-lookup"><span data-stu-id="f5edf-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="f5edf-118">Cada proxy de interfaz puede existir en un archivo DLL independiente que se carga cuando la interfaz que admite se materializa en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f5edf-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="f5edf-119">Estructura del proxy</span><span class="sxs-lookup"><span data-stu-id="f5edf-119">Structure of the Proxy</span></span>

<span data-ttu-id="f5edf-120">En el diagrama siguiente se muestra la estructura de un proxy que admite la serialización estándar de parámetros que pertenecen a dos interfaces: IA1 y IA2.</span><span class="sxs-lookup"><span data-stu-id="f5edf-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="f5edf-121">Cada proxy de interfaz implementa [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) para la comunicación interna entre las partes agregadas.</span><span class="sxs-lookup"><span data-stu-id="f5edf-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="f5edf-122">Cuando el proxy está listo para pasar sus parámetros de cálculo de referencias en el límite del proceso, llama a los métodos de la interfaz [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , que se implementa mediante el canal.</span><span class="sxs-lookup"><span data-stu-id="f5edf-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="f5edf-123">A su vez, el canal reenvía la llamada a la biblioteca en tiempo de ejecución de RPC para que pueda llegar a su destino en el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5edf-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Diagrama que muestra la estructura del proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="f5edf-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5edf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5edf-126">Canal</span><span class="sxs-lookup"><span data-stu-id="f5edf-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="f5edf-127">Comunicación entre objetos</span><span class="sxs-lookup"><span data-stu-id="f5edf-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="f5edf-128">Detalles de serialización</span><span class="sxs-lookup"><span data-stu-id="f5edf-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="f5edf-129">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="f5edf-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="f5edf-130">Stub</span><span class="sxs-lookup"><span data-stu-id="f5edf-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 