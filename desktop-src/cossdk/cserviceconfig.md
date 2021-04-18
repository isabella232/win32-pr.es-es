---
description: Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a CoCreateActivity o CoEnterServiceDomain.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Clase CServiceConfig (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705271"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="2e325-103">Clase CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="2e325-103">CServiceConfig class</span></span>

<span data-ttu-id="2e325-104">Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span><span class="sxs-lookup"><span data-stu-id="2e325-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2e325-105">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="2e325-105">When to implement</span></span>

<span data-ttu-id="2e325-106">Esta clase se implementa mediante COM+.</span><span class="sxs-lookup"><span data-stu-id="2e325-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2e325-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e325-107">Requirement</span></span> | <span data-ttu-id="2e325-108">Value</span><span class="sxs-lookup"><span data-stu-id="2e325-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e325-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="2e325-109">CLSID</span></span>      | <span data-ttu-id="2e325-110">CLSID \_ CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="2e325-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2e325-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="2e325-111">ProgID</span></span>     | <span data-ttu-id="2e325-112">L "COMSVCS. CServiceConfig"</span><span class="sxs-lookup"><span data-stu-id="2e325-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2e325-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2e325-113">Interfaces</span></span> | [<span data-ttu-id="2e325-114">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="2e325-115">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="2e325-116">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="2e325-117">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="2e325-118">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="2e325-119">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="2e325-120">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="2e325-121">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="2e325-122">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="2e325-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="2e325-123">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="2e325-123">When to use</span></span>

<span data-ttu-id="2e325-124">Utilice esta clase para configurar los servicios que desea usar.</span><span class="sxs-lookup"><span data-stu-id="2e325-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="2e325-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) y [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) permiten usar los servicios configurados por esta clase sin necesidad de asociar esos servicios a un componente antes de usarlos.</span><span class="sxs-lookup"><span data-stu-id="2e325-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="2e325-126">Esta clase no está diseñada para utilizarse en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2e325-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e325-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e325-127">Remarks</span></span>

<span data-ttu-id="2e325-128">Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="2e325-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="2e325-129">Los objetos de los que se ha creado una instancia de la clase **CServiceConfig** agregan el contador de referencias de subprocesamiento libre para que puedan almacenarse en tiempo de ejecución del sistema y reutilizarse en distintos apartamentos.</span><span class="sxs-lookup"><span data-stu-id="2e325-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="2e325-130">Para configurar un servicio individual, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz asociada con el servicio y, a continuación, llame a los métodos de esa interfaz para establecer la configuración adecuada.</span><span class="sxs-lookup"><span data-stu-id="2e325-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e325-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e325-131">Requirements</span></span>



| <span data-ttu-id="2e325-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e325-132">Requirement</span></span> | <span data-ttu-id="2e325-133">Value</span><span class="sxs-lookup"><span data-stu-id="2e325-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e325-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e325-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2e325-135">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e325-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2e325-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e325-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2e325-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e325-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2e325-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e325-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e325-139"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e325-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e325-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e325-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e325-141">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="2e325-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="2e325-142">**CoCreateFreeThreadedMarshaler**</span><span class="sxs-lookup"><span data-stu-id="2e325-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="2e325-143">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="2e325-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="2e325-144">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="2e325-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="2e325-145">Servicios COM+ sin componentes</span><span class="sxs-lookup"><span data-stu-id="2e325-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

