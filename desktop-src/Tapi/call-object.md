---
description: El objeto Call representa una conexión de direcciones entre la dirección local y una o varias direcciones.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Call (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678571"
---
# <a name="call-object"></a><span data-ttu-id="ce5b4-103">Call (objeto)</span><span class="sxs-lookup"><span data-stu-id="ce5b4-103">Call Object</span></span>

<span data-ttu-id="ce5b4-104">El objeto Call representa la conexión de una dirección entre la dirección local y una o varias direcciones.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="ce5b4-105">Todo el control de llamada se realiza a través del objeto Call.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-105">All call control is done through the Call object.</span></span> <span data-ttu-id="ce5b4-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) y [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) son las interfaces que se usan con más frecuencia en el objeto Call.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="ce5b4-107">Estas interfaces implementan una variedad de operaciones y consultas, como la adquisición de punteros de interfaz para flujos multimedia o la obtención del identificador del llamador.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="ce5b4-108">Consulte las secciones de información general principales sobre [operaciones de sesión](session-operations-ovr.md) e [información de sesión](session-information-ovr.md) para ver las revisiones de los compatibles con TAPI.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="ce5b4-109">Un proveedor de servicios multimedia puede implementar [interfaces específicas del proveedor](provider-specific-interfaces.md), que se agregan a un objeto de llamada por TAPI.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="ce5b4-110">Para obtener información detallada sobre lo que un proveedor ha implementado, consulte la documentación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="ce5b4-111">En los ejemplos de [creación de una llamada](make-a-call.md) y [recepción de un](receive-a-call.md) código de llamada se muestran algunas ilustraciones del uso de un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="ce5b4-112">Vea [llamar a interfaces de objeto](call-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="ce5b4-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



