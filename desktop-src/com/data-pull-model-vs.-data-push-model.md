---
title: Modelo de Data-Pull y modelo de Data-Push
description: Modelo de Data-Pull y modelo de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421489"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="ba4b9-103">Modelo de Data-Pull y modelo de Data-Push</span><span class="sxs-lookup"><span data-stu-id="ba4b9-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="ba4b9-104">Un cliente de un moniker asincrónico puede elegir entre un modelo de extracción de datos y de inserción de datos para impulsar una operación [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrónica y recibir notificaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="ba4b9-105">En el modelo de extracción de datos, el cliente controla la operación de enlace y el moniker proporciona datos al cliente solo a medida que se leen.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="ba4b9-106">En otras palabras, después de la primera llamada a [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), el moniker no proporciona ningún dato al cliente a menos que el cliente haya consumido todos los datos que ya están disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="ba4b9-107">Dado que los datos se descargan solo cuando se solicita, los clientes que eligen el modelo de extracción de datos deben asegurarse de leer estos datos a tiempo.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="ba4b9-108">En el caso de las descargas de Internet con [monikers URL](url-monikers.md), se puede producir un error en la operación de enlace si un cliente espera demasiado tiempo antes de solicitar más datos.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="ba4b9-109">En el modelo de extracción de datos, el moniker controla la operación de enlace asincrónica y notifica continuamente al cliente cada vez que haya nuevos datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="ba4b9-110">El cliente puede elegir si desea leer los datos en cualquier momento durante la operación de enlace, pero el moniker hará que la operación de enlace se complete sin tener en consideración.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="ba4b9-111">Además, debe recordar seguir las reglas COM para la asignación de memoria cuando se usan monikers asincrónicos, específicamente los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ba4b9-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="ba4b9-112">Siempre que una llamada de función o interfaz COM devuelve un búfer (cadena u otro) a su cliente, el cliente es responsable de liberar la memoria mediante una llamada a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="ba4b9-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="ba4b9-113">Siempre que una interfaz o función COM requiere un búfer de su cliente, el cliente debe asignar ese búfer mediante [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) y el destinatario debe liberarlo.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="ba4b9-114">Asegúrese de seguir estas reglas al asignar las cadenas o los búferes que se pasan a los monikers asincrónicos y recuerde liberar la memoria devuelta por los monikers asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="ba4b9-115">Consulte [Administración](the-com-library.md) de la asignación de memoria y temas relacionados para obtener detalles completos.</span><span class="sxs-lookup"><span data-stu-id="ba4b9-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba4b9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba4b9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4b9-117">Monikers asincrónicos</span><span class="sxs-lookup"><span data-stu-id="ba4b9-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 