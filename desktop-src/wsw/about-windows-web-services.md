---
title: Acerca de los servicios Web de Windows
description: La API de servicios Web de Windows es una API en capas y se puede mostrar como se indica a continuación.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566041"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="e8828-103">Acerca de los servicios Web de Windows</span><span class="sxs-lookup"><span data-stu-id="e8828-103">About Windows Web Services</span></span>

<span data-ttu-id="e8828-104">La API de servicios Web de Windows es una API en capas y se puede ilustrar del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="e8828-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![Diagrama que muestra las capas y las áreas de capas cruzadas de la API de servicios Web de Windows.](images/apistack.png)

<span data-ttu-id="e8828-106">WWSAPI es una API en capas.</span><span class="sxs-lookup"><span data-stu-id="e8828-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="e8828-107">Esperamos que la mayoría de los desarrolladores tengan como destino el modelo de servicio, que es un modelo de programación basado en métodos.</span><span class="sxs-lookup"><span data-stu-id="e8828-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="e8828-108">En el modelo de servicio, el host de servicio proporciona el modelo de programación del lado servidor, mientras que el proxy de servicio proporciona el modelo de programación del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="e8828-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="e8828-109">Cada capa expone un conjunto de API y tipos que se pueden usar con las API de esa capa.</span><span class="sxs-lookup"><span data-stu-id="e8828-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="e8828-110">Modelo de servicio</span><span class="sxs-lookup"><span data-stu-id="e8828-110">Service Model</span></span>

<span data-ttu-id="e8828-111">La capa de nivel superior denominada [modelo de servicio](service-model-layer-overview.md) proporciona un modelo de programación basado en métodos y es el modelo más sencillo de usar.</span><span class="sxs-lookup"><span data-stu-id="e8828-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="e8828-112">En el modelo de servicio, el [host de servicio](service-host.md) proporciona el modelo de programación del lado servidor, mientras que el proxy de [servicio](service-proxy.md) proporciona el modelo de programación del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="e8828-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="e8828-113">El [contexto](context.md) se usa en el modelo de servicio para pasar un estado relevante disponible para la operación de servicio y/o la devolución de llamada cuando se invoca.</span><span class="sxs-lookup"><span data-stu-id="e8828-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="e8828-114">Y el [contrato de servicio](contract.md) se usa para especificar un contrato de servicio en un extremo expuesto en el servicio.</span><span class="sxs-lookup"><span data-stu-id="e8828-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="e8828-115">Los siguientes componentes y operaciones forman parte del nivel de servicio:</span><span class="sxs-lookup"><span data-stu-id="e8828-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="e8828-116">Host de servicio</span><span class="sxs-lookup"><span data-stu-id="e8828-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="e8828-117">Proxy de servicio</span><span class="sxs-lookup"><span data-stu-id="e8828-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="e8828-118">Contexto</span><span class="sxs-lookup"><span data-stu-id="e8828-118">Context</span></span>](context.md)
-   [<span data-ttu-id="e8828-119">DataContract</span><span class="sxs-lookup"><span data-stu-id="e8828-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="e8828-120">Metadatos de servicio</span><span class="sxs-lookup"><span data-stu-id="e8828-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="e8828-121">Nivel de canal</span><span class="sxs-lookup"><span data-stu-id="e8828-121">Channel Layer</span></span>

<span data-ttu-id="e8828-122">El modelo de servicio se basa en una capa de canal, lo que proporciona una flexibilidad completa, pero es más difícil de usar.</span><span class="sxs-lookup"><span data-stu-id="e8828-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="e8828-123">Los siguientes componentes y operaciones forman parte de la capa del canal:</span><span class="sxs-lookup"><span data-stu-id="e8828-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="e8828-124">Message</span><span class="sxs-lookup"><span data-stu-id="e8828-124">Message</span></span>](message.md)
-   [<span data-ttu-id="e8828-125">Canal</span><span class="sxs-lookup"><span data-stu-id="e8828-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="e8828-126">Agente de escucha</span><span class="sxs-lookup"><span data-stu-id="e8828-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="e8828-127">Errores</span><span class="sxs-lookup"><span data-stu-id="e8828-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="e8828-128">Url</span><span class="sxs-lookup"><span data-stu-id="e8828-128">Url</span></span>](url.md)
-   [<span data-ttu-id="e8828-129">Seguridad</span><span class="sxs-lookup"><span data-stu-id="e8828-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="e8828-130">Importación de metadatos</span><span class="sxs-lookup"><span data-stu-id="e8828-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="e8828-131">Nivel XML</span><span class="sxs-lookup"><span data-stu-id="e8828-131">XML Layer</span></span>

<span data-ttu-id="e8828-132">La capa de canales a su vez se basa en un marco XML ligero, que incluye la deserialización de los tipos de datos de C.</span><span class="sxs-lookup"><span data-stu-id="e8828-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="e8828-133">Los siguientes componentes y operaciones forman parte de la capa XML:</span><span class="sxs-lookup"><span data-stu-id="e8828-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="e8828-134">Escritor XML</span><span class="sxs-lookup"><span data-stu-id="e8828-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="e8828-135">Lector XML</span><span class="sxs-lookup"><span data-stu-id="e8828-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="e8828-136">Búfer XML</span><span class="sxs-lookup"><span data-stu-id="e8828-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="e8828-137">Serialización</span><span class="sxs-lookup"><span data-stu-id="e8828-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="e8828-138">Compatibilidad con el lenguaje XML</span><span class="sxs-lookup"><span data-stu-id="e8828-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="e8828-139">Común a todas las capas</span><span class="sxs-lookup"><span data-stu-id="e8828-139">Common to all layers</span></span>

<span data-ttu-id="e8828-140">A continuación se muestran los temas que se aplican a cualquiera de las tres capas:</span><span class="sxs-lookup"><span data-stu-id="e8828-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="e8828-141">Errores</span><span class="sxs-lookup"><span data-stu-id="e8828-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="e8828-142">Modelo asincrónico</span><span class="sxs-lookup"><span data-stu-id="e8828-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="e8828-143">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="e8828-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="e8828-144">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="e8828-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="e8828-145">Cancelación</span><span class="sxs-lookup"><span data-stu-id="e8828-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="e8828-146">Utilidades</span><span class="sxs-lookup"><span data-stu-id="e8828-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="e8828-147">Depuración</span><span class="sxs-lookup"><span data-stu-id="e8828-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="e8828-148">Herramienta del compilador Wsutil</span><span class="sxs-lookup"><span data-stu-id="e8828-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="e8828-149">Montón</span><span class="sxs-lookup"><span data-stu-id="e8828-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="e8828-150">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8828-150">Examples</span></span>

<span data-ttu-id="e8828-151">Para obtener más información sobre los elementos de la API, consulte [referencia de servicios Web de Windows](windows-web-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e8828-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="e8828-152">Para obtener ejemplos del uso de la API, vea [uso de servicios Web de Windows](using-windows-web-services.md).</span><span class="sxs-lookup"><span data-stu-id="e8828-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




