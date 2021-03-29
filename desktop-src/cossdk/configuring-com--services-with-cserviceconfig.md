---
description: Configuración de servicios COM+ con CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configuración de servicios COM+ con CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807189"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="77c71-103">Configuración de servicios COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="77c71-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="77c71-104">La clase [**CServiceConfig**](cserviceconfig.md) se utiliza para configurar los servicios com+ que se pueden usar sin componentes.</span><span class="sxs-lookup"><span data-stu-id="77c71-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="77c71-105">Agrega el contador de referencias de subprocesamiento libre, por lo que se puede usar en distintos apartamentos.</span><span class="sxs-lookup"><span data-stu-id="77c71-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="77c71-106">Para configurar un servicio individual, debe llamar a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz asociada con el servicio y, a continuación, llamar a los métodos de esa interfaz para establecer la configuración adecuada.</span><span class="sxs-lookup"><span data-stu-id="77c71-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="77c71-107">En la tabla siguiente se describen las interfaces que se implementan a través de la clase **CServiceConfig** .</span><span class="sxs-lookup"><span data-stu-id="77c71-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="77c71-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="77c71-108">Interface</span></span>                                                                         | <span data-ttu-id="77c71-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="77c71-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77c71-110">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="77c71-111">La interfaz predeterminada para la clase.</span><span class="sxs-lookup"><span data-stu-id="77c71-111">The default interface for the class.</span></span> <span data-ttu-id="77c71-112">Se usa para inicializar rápidamente muchos de los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="77c71-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="77c71-113">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="77c71-114">Se utiliza para configurar la información intrínseca del integrador de transacciones COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="77c71-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="77c71-115">COMTI permite a los desarrolladores integrar programas de transacciones basados en un gran sistema (mainframe) con aplicaciones basadas en componentes.</span><span class="sxs-lookup"><span data-stu-id="77c71-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="77c71-116">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="77c71-117">Se utiliza para configurar la información intrínseca de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="77c71-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="77c71-118">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="77c71-119">Se utiliza para configurar el modo en que se usan las particiones COM+ con los servicios.</span><span class="sxs-lookup"><span data-stu-id="77c71-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="77c71-120">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="77c71-121">Se utiliza para configurar ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="77c71-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="77c71-122">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="77c71-123">Se utiliza para configurar los servicios de sincronización de COM+.</span><span class="sxs-lookup"><span data-stu-id="77c71-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="77c71-124">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="77c71-125">Se utiliza para configurar el grupo de subprocesos para el servicio COM+.</span><span class="sxs-lookup"><span data-stu-id="77c71-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="77c71-126">El grupo de subprocesos solo se puede configurar cuando se usa la función [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .</span><span class="sxs-lookup"><span data-stu-id="77c71-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="77c71-127">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="77c71-128">Se usa para configurar la propiedad Tracker.</span><span class="sxs-lookup"><span data-stu-id="77c71-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="77c71-129">Tracker es un mecanismo de informes que usa el código de supervisión para ver qué código se está ejecutando cuando.</span><span class="sxs-lookup"><span data-stu-id="77c71-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="77c71-130">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="77c71-131">Se utiliza para configurar el servicio de transacciones de COM+.</span><span class="sxs-lookup"><span data-stu-id="77c71-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="77c71-132">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="77c71-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="77c71-133">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="77c71-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="77c71-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="77c71-134">Visual Basic</span></span>

<span data-ttu-id="77c71-135">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="77c71-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="77c71-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="77c71-136">C/C++</span></span>

<span data-ttu-id="77c71-137">En el siguiente fragmento de código se muestra cómo crear y configurar un objeto [**CServiceConfig**](cserviceconfig.md) para utilizar transacciones com+.</span><span class="sxs-lookup"><span data-stu-id="77c71-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="77c71-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77c71-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c71-139">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="77c71-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="77c71-140">Usar los servicios COM+ a través de CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="77c71-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="77c71-141">Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="77c71-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

