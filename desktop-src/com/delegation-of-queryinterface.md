---
title: Delegación de QueryInterface
description: Delegación de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149653"
---
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="32632-103">Delegación de QueryInterface</span><span class="sxs-lookup"><span data-stu-id="32632-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="32632-104">Los controladores que requieren acceso a algunas de las interfaces internas en el administrador del proxy deben pasar por la interfaz [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) .</span><span class="sxs-lookup"><span data-stu-id="32632-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="32632-105">Esto evita que los controladores deleguen y expongan de forma ciega las interfaces internas del agregado fuera del agregado.</span><span class="sxs-lookup"><span data-stu-id="32632-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="32632-106">Estas interfaces incluyen [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) y [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="32632-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="32632-107">Si el controlador desea exponer **IClientSecurity** o **IMultiQI**, debe implementarlos.</span><span class="sxs-lookup"><span data-stu-id="32632-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="32632-108">En el caso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), si el cliente intenta establecer la seguridad en una interfaz expuesta por el controlador, el controlador debe establecer la seguridad en el proxy de la interfaz de red subyacente.</span><span class="sxs-lookup"><span data-stu-id="32632-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="32632-109">En el caso de [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), el controlador debe rellenar las interfaces que conoce y, a continuación, reenviar la llamada al administrador de proxy para obtener el resto de las interfaces rellenadas.</span><span class="sxs-lookup"><span data-stu-id="32632-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32632-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32632-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32632-111">Controlador de Client-Side ligero</span><span class="sxs-lookup"><span data-stu-id="32632-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 