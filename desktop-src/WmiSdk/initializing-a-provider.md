---
description: Una de las primeras tareas que debe codificar para un proveedor es el proceso de inicialización, que cubre todas las tareas que debe realizar el proveedor y que le permite enviar y recibir información de WMI, controlar un objeto administrado y realizar otras tareas.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inicializar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913369"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="2e18e-103">Inicializar un proveedor</span><span class="sxs-lookup"><span data-stu-id="2e18e-103">Initializing a Provider</span></span>

<span data-ttu-id="2e18e-104">Una de las primeras tareas que debe codificar para un proveedor es el proceso de inicialización, que cubre todas las tareas que debe realizar el proveedor y que le permite enviar y recibir información de WMI, controlar un objeto administrado y realizar otras tareas.</span><span class="sxs-lookup"><span data-stu-id="2e18e-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="2e18e-105">Cada tipo de proveedor tiene un conjunto diferente de tareas que debe realizar y tiene un conjunto de interfaces únicas que acompañan.</span><span class="sxs-lookup"><span data-stu-id="2e18e-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="2e18e-106">Sin embargo, todos los proveedores se inicializan a través de la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informan a WMI de su estado de inicialización a través de la interfaz [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .</span><span class="sxs-lookup"><span data-stu-id="2e18e-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="2e18e-107">En el procedimiento siguiente se describe cómo inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e18e-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="2e18e-108">**Para inicializar un proveedor**</span><span class="sxs-lookup"><span data-stu-id="2e18e-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="2e18e-109">Implemente [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) para su proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e18e-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="2e18e-110">Cuando WMI determina que un cliente requiere los servicios de un proveedor, WMI carga el proveedor llamando al método [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="2e18e-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="2e18e-111">Implemente las interfaces exclusivas del tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e18e-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="2e18e-112">Informe a WMI de que el proveedor ha terminado con la inicialización mediante una llamada a [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="2e18e-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="2e18e-113">Todas las implementaciones de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deben llamar a [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para notificar el estado de inicialización a WMI.</span><span class="sxs-lookup"><span data-stu-id="2e18e-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="2e18e-114">El método **SetStatus** permite a WMI determinar si un proveedor está listo para recibir solicitudes y el tipo de solicitudes que el proveedor está listo para recibir.</span><span class="sxs-lookup"><span data-stu-id="2e18e-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="2e18e-115">En el procedimiento siguiente se describe cómo notificar una inicialización correcta.</span><span class="sxs-lookup"><span data-stu-id="2e18e-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="2e18e-116">**Para notificar una inicialización correcta**</span><span class="sxs-lookup"><span data-stu-id="2e18e-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="2e18e-117">Establezca el parámetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) en **WBEM \_ S \_ inicializado**.</span><span class="sxs-lookup"><span data-stu-id="2e18e-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="2e18e-118">Al devolver **WBEM \_ S \_ inicializado**, un proveedor indica una preparación para controlar las solicitudes de aplicaciones, WMI y otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="2e18e-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="2e18e-119">Después de haber \_ \_ inicializado WBEM S, WMI realiza una llamada al método [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e18e-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="2e18e-120">Esta consulta recupera un puntero a la interfaz principal del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e18e-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="2e18e-121">En el procedimiento siguiente se describe cómo notificar un error durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="2e18e-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="2e18e-122">**Para notificar un error durante la inicialización**</span><span class="sxs-lookup"><span data-stu-id="2e18e-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="2e18e-123">Establezca el parámetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) en **WBEM \_ E \_**.</span><span class="sxs-lookup"><span data-stu-id="2e18e-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="2e18e-124">Los proveedores de vistas de WMI que devuelven **WBEM \_ E \_ no** funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e18e-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="2e18e-125">WMI libera el puntero [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) después de que WMI haya obtenido un puntero a la interfaz principal del proveedor o después de que se haya producido un error en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="2e18e-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e18e-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e18e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e18e-127">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="2e18e-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="2e18e-128">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="2e18e-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="2e18e-129">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="2e18e-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



