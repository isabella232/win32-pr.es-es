---
title: Agrupa
description: El código auxiliar, al igual que el proxy, se compone de una o varias partes de la interfaz y un administrador.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105697898"
---
# <a name="stub"></a><span data-ttu-id="1c3ef-103">Agrupa</span><span class="sxs-lookup"><span data-stu-id="1c3ef-103">Stub</span></span>

<span data-ttu-id="1c3ef-104">El código auxiliar, al igual que el proxy, se compone de una o varias partes de la interfaz y un administrador.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="1c3ef-105">Cada código auxiliar de interfaz proporciona código para deshacer las referencias de los parámetros y el código que llama a una de las interfaces admitidas del objeto.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="1c3ef-106">Cada código auxiliar también proporciona una interfaz para la comunicación interna.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="1c3ef-107">El administrador de código auxiliar realiza un seguimiento de los códigos auxiliares de interfaz disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="1c3ef-108">Sin embargo, hay las siguientes diferencias entre el código auxiliar y el proxy:</span><span class="sxs-lookup"><span data-stu-id="1c3ef-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="1c3ef-109">La diferencia más importante es que el código auxiliar representa el cliente en el espacio de direcciones del objeto.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="1c3ef-110">El código auxiliar no se implementa como un objeto agregado porque no hay ningún requisito de que el cliente se pueda ver como una sola unidad; cada parte del código auxiliar es un componente independiente.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="1c3ef-111">Los códigos auxiliares de la interfaz son privados en lugar de públicos.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="1c3ef-112">El código auxiliar de la interfaz implementa [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), no [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span><span class="sxs-lookup"><span data-stu-id="1c3ef-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="1c3ef-113">En lugar de empaquetar los parámetros que se van a serializar, el código auxiliar los desempaquetará después de que se hayan calculado y, a continuación, empaquetará la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="1c3ef-114">Estructura del código auxiliar</span><span class="sxs-lookup"><span data-stu-id="1c3ef-114">Structure of the Stub</span></span>

<span data-ttu-id="1c3ef-115">En el diagrama siguiente se muestra la estructura del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="1c3ef-116">Cada código auxiliar de interfaz está conectado a una interfaz en el objeto.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="1c3ef-117">El canal envía los mensajes entrantes al código auxiliar de la interfaz correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="1c3ef-118">Todos los componentes se comunican con el canal a través de [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), la interfaz que proporciona acceso a la biblioteca en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="1c3ef-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Captura de pantalla que muestra la estructura del código auxiliar.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="1c3ef-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c3ef-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c3ef-121">Canal</span><span class="sxs-lookup"><span data-stu-id="1c3ef-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="1c3ef-122">Comunicación entre objetos</span><span class="sxs-lookup"><span data-stu-id="1c3ef-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="1c3ef-123">Detalles de serialización</span><span class="sxs-lookup"><span data-stu-id="1c3ef-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="1c3ef-124">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="1c3ef-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="1c3ef-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="1c3ef-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 