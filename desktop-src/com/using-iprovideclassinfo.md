---
title: Usar IProvideClassInfo
description: Usar IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078441"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="662af-103">Usar IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="662af-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="662af-104">Un objeto conectable puede ofrecer las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) y [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que sus clientes puedan examinar fácilmente su información de tipo.</span><span class="sxs-lookup"><span data-stu-id="662af-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="662af-105">Esta capacidad es importante cuando se trabaja con interfaces salientes, que, por definición, se definen mediante un objeto, pero se implementa mediante un cliente en su propio objeto receptor.</span><span class="sxs-lookup"><span data-stu-id="662af-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="662af-106">En algunos casos, una interfaz de salida se conoce en tiempo de compilación para el objeto conectable y el objeto receptor. Este es el caso con [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="662af-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="662af-107">En otros casos, sin embargo, solo el objeto conectable conoce sus definiciones de interfaz de salida en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="662af-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="662af-108">En estos casos, el cliente debe obtener la información de tipo de la interfaz de salida para que pueda proporcionar dinámicamente un receptor que admita los puntos de entrada correctos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="662af-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="662af-109">El cliente enumera los puntos de conexión y, a continuación, para obtener los IID de las interfaces salientes admitidas por el objeto conectable, llama a [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="662af-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="662af-110">El cliente consulta el objeto conectable para una de las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="662af-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="662af-111">El cliente llama a los métodos de las interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obtener la información de tipo de la interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="662af-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="662af-112">El cliente crea un objeto receptor que admite la interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="662af-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="662af-113">El proceso continúa y el cliente llama a [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar su receptor al punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="662af-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="662af-114">En la información de tipo, el [**origen**](/windows/desktop/Midl/source) del atributo marca una [**interfaz**](/windows/desktop/Midl/interface) o [**dispinterface**](/windows/desktop/Midl/dispinterface) que aparece bajo una [**coclase**](/windows/desktop/Midl/coclass) como una interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="662af-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="662af-115">Los que aparecen sin este atributo se consideran interfaces entrantes.</span><span class="sxs-lookup"><span data-stu-id="662af-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="662af-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="662af-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="662af-117">Interfaces de objeto conectables</span><span class="sxs-lookup"><span data-stu-id="662af-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="662af-118">Proporcionar información de clase</span><span class="sxs-lookup"><span data-stu-id="662af-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 