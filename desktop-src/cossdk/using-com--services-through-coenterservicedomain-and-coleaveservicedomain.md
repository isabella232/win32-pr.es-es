---
description: Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153254"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="675ee-103">Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="675ee-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="675ee-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) se usan juntos para rodear un área de código que se ejecuta en su propio contexto y puede usar los servicios com+ sin necesidad de componentes com+.</span><span class="sxs-lookup"><span data-stu-id="675ee-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="675ee-105">Los servicios COM+ que se usan en este contexto se configuran mediante el objeto [**CServiceConfig**](cserviceconfig.md) que se pasa a **CoEnterServiceDomain**.</span><span class="sxs-lookup"><span data-stu-id="675ee-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="675ee-106">El código que está rodeado por **CoEnterServiceDomain** y **CoLeaveServiceDomain** se comporta como si fuera un método al que se llama en un objeto creado dentro de este contexto.</span><span class="sxs-lookup"><span data-stu-id="675ee-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="675ee-107">Una aplicación de scripting puede usar este par de funciones para proporcionar compatibilidad en tiempo de ejecución de los servicios COM+ sin componentes.</span><span class="sxs-lookup"><span data-stu-id="675ee-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="675ee-108">Por ejemplo, se puede desarrollar una aplicación de scripting para proporcionar etiquetas que permitan a los escritores de scripts entrar y salir de un dominio de servicio dentro del script.</span><span class="sxs-lookup"><span data-stu-id="675ee-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="675ee-109">Cuando el motor de scripting procesa el script y encuentra las etiquetas, puede llamar a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) con un objeto [**CServiceConfig**](cserviceconfig.md) preconfigurado, ejecutar el código necesario y, después, llamar a [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="675ee-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="675ee-110">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="675ee-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="675ee-111">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="675ee-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="675ee-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="675ee-112">Visual Basic</span></span>

<span data-ttu-id="675ee-113">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="675ee-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="675ee-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="675ee-114">C/C++</span></span>

<span data-ttu-id="675ee-115">En el fragmento de código siguiente se muestra cómo usar los servicios COM+ entre las llamadas a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="675ee-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="675ee-116">Con el fin de ser breves se omite el control de errores.</span><span class="sxs-lookup"><span data-stu-id="675ee-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="675ee-117">Este fragmento de código usa el objeto [**CServiceConfig**](cserviceconfig.md) que se creó y configuró en configuración de los [servicios com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="675ee-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="675ee-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="675ee-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="675ee-119">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="675ee-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="675ee-120">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="675ee-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="675ee-121">Configuración de servicios COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="675ee-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="675ee-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="675ee-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="675ee-123">Usar los servicios COM+ a través de CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="675ee-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



