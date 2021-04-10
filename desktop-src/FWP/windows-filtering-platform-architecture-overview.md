---
title: Arquitectura de WFP
description: En esta sección se proporciona una breve introducción a la arquitectura de la plataforma de filtrado de Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271194"
---
# <a name="wfp-architecture"></a><span data-ttu-id="80cf4-103">Arquitectura de WFP</span><span class="sxs-lookup"><span data-stu-id="80cf4-103">WFP Architecture</span></span>

<span data-ttu-id="80cf4-104">En la siguiente ilustración se muestra la arquitectura básica de la plataforma de filtrado de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="80cf4-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![arquitectura básica del diagrama de la plataforma de filtrado de Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="80cf4-106">Motor de filtro</span><span class="sxs-lookup"><span data-stu-id="80cf4-106">Filter Engine</span></span>

<span data-ttu-id="80cf4-107">El motor de filtro contiene un componente de modo de usuario y un componente de modo kernel, que, en conjunto, realizan todas las operaciones de filtrado en los datos de red.</span><span class="sxs-lookup"><span data-stu-id="80cf4-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="80cf4-108">El motor de filtro contiene varias capas de filtrado que se asignan de forma flexible a las capas de la pila de red del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="80cf4-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="80cf4-109">Las capas del motor de filtros se dividen en capas en modo de usuario y en capas en modo kernel basadas en el componente del motor de filtro que las posee.</span><span class="sxs-lookup"><span data-stu-id="80cf4-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="80cf4-110">El componente de modo de usuario realiza el filtrado de RPC y IPsec.</span><span class="sxs-lookup"><span data-stu-id="80cf4-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="80cf4-111">El motor de filtro contiene aproximadamente 10 niveles de filtrado de modo usuario.</span><span class="sxs-lookup"><span data-stu-id="80cf4-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="80cf4-112">El componente de modo kernel realiza el filtrado en los niveles de red y transporte de la pila TC/IP.</span><span class="sxs-lookup"><span data-stu-id="80cf4-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="80cf4-113">Este componente también llama a las funciones de llamada disponibles durante el proceso de [clasificación](basic-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="80cf4-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="80cf4-114">El motor de filtro contiene aproximadamente 50 capas de filtrado de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="80cf4-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="80cf4-115">Consulte [**filtrado de los identificadores de capas**](management-filtering-layer-identifiers-.md) para obtener una descripción de cada una de las capas del motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="80cf4-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="80cf4-116">Motor de filtrado de base</span><span class="sxs-lookup"><span data-stu-id="80cf4-116">Base Filtering Engine</span></span>

<span data-ttu-id="80cf4-117">El motor de filtrado de base (BFE) es un servicio de modo de usuario (bfe.dll que se ejecuta en un proceso de svchost.exe) que coordina los componentes de WFP.</span><span class="sxs-lookup"><span data-stu-id="80cf4-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="80cf4-118">Las tareas principales realizadas por BFE son la adición y eliminación de filtros del sistema, el almacenamiento de la configuración del filtro y la aplicación de la seguridad de configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="80cf4-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="80cf4-119">Las aplicaciones se comunican con BFE a través de las [funciones de administración de WFP](fwp-mgmt-functions.md).</span><span class="sxs-lookup"><span data-stu-id="80cf4-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="80cf4-120">Controladores de llamadas</span><span class="sxs-lookup"><span data-stu-id="80cf4-120">Callout Drivers</span></span>

<span data-ttu-id="80cf4-121">Los controladores de llamadas proporcionan funcionalidad de filtrado adicional mediante la adición de funciones de llamada personalizadas al motor de filtro en uno o varios de los niveles de filtrado del modo kernel.</span><span class="sxs-lookup"><span data-stu-id="80cf4-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="80cf4-122">Las llamadas admiten inspección profunda y paquetes, así como la modificación de secuencias.</span><span class="sxs-lookup"><span data-stu-id="80cf4-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="80cf4-123">Una vez que un controlador de llamada ha agregado sus funciones de llamada al motor de filtro, los filtros que especifican la función de llamada de un controlador determinado se pueden agregar al proceso de filtrado.</span><span class="sxs-lookup"><span data-stu-id="80cf4-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="80cf4-124">Estos filtros se pueden agregar mediante una aplicación de administración de modo de usuario o el propio controlador de llamada.</span><span class="sxs-lookup"><span data-stu-id="80cf4-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="80cf4-125">La interfaz de modo kernel, proporcionada en el kit de desarrollo de Windows, solo se debe usar cuando sea necesario y no como sustituto de la API de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="80cf4-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="80cf4-126">Para obtener más información sobre los controladores de llamadas, consulte la sección sobre la plataforma de filtrado de Windows del [Kit de desarrollo de Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="80cf4-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="80cf4-127">La plataforma de filtrado de Windows incluye una serie de funciones de llamada integradas que se pueden usar para la comunicación de datos segura de IPsec, la configuración de filtrado con estado y el filtrado de modo oculto.</span><span class="sxs-lookup"><span data-stu-id="80cf4-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="80cf4-128">Vea [**identificadores de llamada integrados**](built-in-callout-identifiers.md) para obtener una lista completa de funciones de llamada integradas.</span><span class="sxs-lookup"><span data-stu-id="80cf4-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80cf4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80cf4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80cf4-130">Modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="80cf4-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="80cf4-131">Operación de WFP</span><span class="sxs-lookup"><span data-stu-id="80cf4-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="80cf4-132">Controladores de llamadas de plataforma de filtrado de Windows: Guía de diseño</span><span class="sxs-lookup"><span data-stu-id="80cf4-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="80cf4-133">Controladores de llamadas de plataforma de filtrado de Windows: referencia</span><span class="sxs-lookup"><span data-stu-id="80cf4-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 