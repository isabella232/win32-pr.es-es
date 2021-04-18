---
description: El asignador de envío se crea mediante COM CoCreateInstance y expone una interfaz, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Asignador de envío
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687514"
---
# <a name="dispatch-mapper"></a><span data-ttu-id="517f9-103">Asignador de envío</span><span class="sxs-lookup"><span data-stu-id="517f9-103">Dispatch Mapper</span></span>

<span data-ttu-id="517f9-104">El asignador de envío se crea mediante COM **CoCreateInstance** y expone una interfaz, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span><span class="sxs-lookup"><span data-stu-id="517f9-104">The Dispatch Mapper is created using COM **CoCreateInstance** and exposes one interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span></span> <span data-ttu-id="517f9-105">Esta interfaz permite a una aplicación recuperar el puntero de envío de otra interfaz en un objeto, dado el puntero de envío de una interfaz y el GUID de otro.</span><span class="sxs-lookup"><span data-stu-id="517f9-105">This interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.</span></span> <span data-ttu-id="517f9-106">Esta interfaz se proporciona para ayudar a los programadores a usar aplicaciones de scripting que no proporcionan un medio para sondear fácilmente las interfaces en un objeto.</span><span class="sxs-lookup"><span data-stu-id="517f9-106">This interface is provided to assist programmers using scripting applications which do not provide a means of readily polling the interfaces on an object.</span></span>

<span data-ttu-id="517f9-107">El asignador de envío utiliza la interfaz **IObjectSafety** del objeto para asegurarse de que el objeto es seguro para el scripting en la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="517f9-107">The Dispatch Mapper uses an object's **IObjectSafety** interface to make sure the object is safe for scripting on the requested interface.</span></span> <span data-ttu-id="517f9-108">Si el objeto no implementa **IObjectSafety**, o si el objeto no es seguro en esta interfaz determinada, se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="517f9-108">If the object does not implement **IObjectSafety**, or if the object is not safe on this particular interface, the call will fail.</span></span>

 

 



