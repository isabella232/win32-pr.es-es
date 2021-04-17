---
description: La función CoCreateActivity se usa para enviar el trabajo por lotes al sistema COM+. Permite que las aplicaciones basadas en scripts admitan una configuración de servicio COM+ de toda la aplicación.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Usar los servicios COM+ a través de CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705367"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="3c073-104">Usar los servicios COM+ a través de CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="3c073-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="3c073-105">La función [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) se usa para enviar el trabajo por lotes al sistema com+.</span><span class="sxs-lookup"><span data-stu-id="3c073-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="3c073-106">Permite que las aplicaciones basadas en scripts admitan una configuración de servicio COM+ de toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3c073-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="3c073-107">Los servicios COM+ deseados se configuran mediante un objeto [**CServiceConfig**](cserviceconfig.md) que se pasa a la función.</span><span class="sxs-lookup"><span data-stu-id="3c073-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="3c073-108">La función crea un objeto de actividad y devuelve la interfaz [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="3c073-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="3c073-109">El trabajo por lotes se puede enviar de forma sincrónica o asincrónica mediante los métodos [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) o [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3c073-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="3c073-110">Un puntero a una interfaz [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) se pasa a cada uno de estos métodos, y el trabajo por lotes lo implementa el desarrollador en el método [**Call**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) de la interfaz **IServiceCall** .</span><span class="sxs-lookup"><span data-stu-id="3c073-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3c073-111">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="3c073-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="3c073-112">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="3c073-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3c073-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3c073-113">Visual Basic</span></span>

<span data-ttu-id="3c073-114">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="3c073-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3c073-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="3c073-115">C/C++</span></span>

<span data-ttu-id="3c073-116">En el fragmento de código siguiente se muestra cómo usar los servicios COM+ a través de [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span><span class="sxs-lookup"><span data-stu-id="3c073-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="3c073-117">Con el fin de ser breves se omite el control de errores.</span><span class="sxs-lookup"><span data-stu-id="3c073-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="3c073-118">Este fragmento de código usa el objeto [**CServiceConfig**](cserviceconfig.md) que se creó y configuró en configuración de los [servicios com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="3c073-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="3c073-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c073-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c073-120">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="3c073-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="3c073-121">Configuración de servicios COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3c073-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="3c073-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="3c073-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="3c073-123">Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="3c073-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



