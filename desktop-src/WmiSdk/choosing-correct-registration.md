---
description: WMI admite diferentes modelos de subprocesos en función de cómo esté hospedado el proveedor y el tipo de funcionalidad del proveedor, como clase o propiedad.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Elección del registro correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716212"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="0249b-103">Elección del registro correcto</span><span class="sxs-lookup"><span data-stu-id="0249b-103">Choosing Correct Registration</span></span>

<span data-ttu-id="0249b-104">WMI admite diferentes modelos de subprocesos en función de cómo esté hospedado el proveedor y el tipo de funcionalidad del proveedor, como [clase](writing-a-class-provider.md) o [propiedad](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0249b-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="0249b-105">Por ejemplo, los [*proveedores desacoplados*](gloss-d.md) no admiten todos los tipos de funcionalidad de proveedor.</span><span class="sxs-lookup"><span data-stu-id="0249b-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="0249b-106">Para obtener más información sobre los diferentes modelos de hospedaje y cómo configurarlos, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="0249b-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="0249b-107">Proveedores de In-Process</span><span class="sxs-lookup"><span data-stu-id="0249b-107">In-Process Providers</span></span>

<span data-ttu-id="0249b-108">Los proveedores en proceso se ejecutan en un proceso de host compartido, Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="0249b-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="0249b-109">La mayoría de los tipos de proveedores en proceso utilizan el modelo de contenedor multiproceso (MTA).</span><span class="sxs-lookup"><span data-stu-id="0249b-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="0249b-110">El modelo MTA es compatible con los siguientes tipos de funcionalidad de proveedor:</span><span class="sxs-lookup"><span data-stu-id="0249b-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="0249b-111">Proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="0249b-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="0249b-112">Proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="0249b-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="0249b-113">Proveedor de método</span><span class="sxs-lookup"><span data-stu-id="0249b-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="0249b-114">Proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="0249b-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="0249b-115">Proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="0249b-116">Proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="0249b-117">El modelo de contenedor uniproceso (STA) es compatible con algunos tipos de funcionalidad de proveedor:</span><span class="sxs-lookup"><span data-stu-id="0249b-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="0249b-118">Proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="0249b-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="0249b-119">Proveedor de método</span><span class="sxs-lookup"><span data-stu-id="0249b-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="0249b-120">Proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="0249b-121">Proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="0249b-122">Proveedores fuera de proceso</span><span class="sxs-lookup"><span data-stu-id="0249b-122">Out-of-Process Providers</span></span>

<span data-ttu-id="0249b-123">Los proveedores que se hospedan en un host de servicio compartido diferente admiten la siguiente funcionalidad de proveedor:</span><span class="sxs-lookup"><span data-stu-id="0249b-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="0249b-124">Proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="0249b-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="0249b-125">Proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="0249b-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="0249b-126">Proveedor de método</span><span class="sxs-lookup"><span data-stu-id="0249b-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="0249b-127">Proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="0249b-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="0249b-128">Proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="0249b-129">Proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="0249b-130">Para obtener más información sobre los hosts de servicios compartidos, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="0249b-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="0249b-131">Proveedores desacoplados</span><span class="sxs-lookup"><span data-stu-id="0249b-131">Decoupled Providers</span></span>

<span data-ttu-id="0249b-132">Los proveedores desacoplados se hospedan en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0249b-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="0249b-133">Para obtener más información, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="0249b-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="0249b-134">Los proveedores creados con WMI en el .NET Framework están desacoplados.</span><span class="sxs-lookup"><span data-stu-id="0249b-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="0249b-135">Los proveedores desacoplados admiten la siguiente funcionalidad de proveedor:</span><span class="sxs-lookup"><span data-stu-id="0249b-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="0249b-136">Proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="0249b-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="0249b-137">Proveedor de método</span><span class="sxs-lookup"><span data-stu-id="0249b-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="0249b-138">Proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="0249b-139">Proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="0249b-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="0249b-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0249b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0249b-141">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="0249b-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="0249b-142">Hospedaje y seguridad de proveedores</span><span class="sxs-lookup"><span data-stu-id="0249b-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



