---
title: Aspectos básicos de la aplicación
description: Aspectos básicos de la aplicación
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK de Windows Media Format, conceptos básicos de la aplicación DRM
- Administración de derechos digitales (DRM), aspectos básicos de la aplicación
- DRM (administración de derechos digitales), aspectos básicos de la aplicación
- Administración de derechos digitales (DRM), función WMDRMStartup
- DRM (administración de derechos digitales), función WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268326"
---
# <a name="application-basics"></a><span data-ttu-id="79b27-109">Aspectos básicos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="79b27-109">Application Basics</span></span>

<span data-ttu-id="79b27-110">Hay algún procesamiento adicional que debe realizar para cualquier aplicación que use las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79b27-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="79b27-111">En este tema se describen los requisitos para una aplicación sencilla.</span><span class="sxs-lookup"><span data-stu-id="79b27-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="79b27-112">En primer lugar, debe inicializar las API extendidas del cliente DRM de Windows Media mediante una llamada a la función [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="79b27-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="79b27-113">Los objetos del SDK son objetos COM, pero no es necesario llamar a **CoIntialize**, porque la función **WMDRMStatup** inicializa com automáticamente.</span><span class="sxs-lookup"><span data-stu-id="79b27-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="79b27-114">El SDK de Windows Media Format solo usa un subconjunto de COM, por lo que si usa objetos COM distintos de los de la API extendida del cliente DRM de Windows Media, debe seguir llamando a **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="79b27-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="79b27-115">Todos los objetos de las API extendidas del cliente DRM de Windows Media se crean mediante funciones y métodos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="79b27-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="79b27-116">Nunca necesita llamar a **CoCreateInstance** para crear un objeto.</span><span class="sxs-lookup"><span data-stu-id="79b27-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="79b27-117">La primera interfaz en la que se crean instancias para cualquier aplicación que use el SDK es [**IWMDRMProvider**](iwmdrmprovider.md), que se puede usar para crear instancias de todas las demás interfaces base.</span><span class="sxs-lookup"><span data-stu-id="79b27-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="79b27-118">Para obtener una instancia de **IWMDRMProvider**, debe llamar a [**WMDRMCreateProvider**](wmdrmcreateprovider.md) o [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span><span class="sxs-lookup"><span data-stu-id="79b27-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="79b27-119">La diferencia entre estas funciones es que **WMDRMCreateProvider** crea un objeto que, a su vez, solo puede crear objetos que no admiten métodos que requieran la biblioteca de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="79b27-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="79b27-120">Después de tener una instancia de **IWMDRMProvider**, puede crear los otros objetos que necesita llamando a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="79b27-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="79b27-121">Cuando esté listo para salir de la aplicación, debe liberar los recursos del subsistema DRM mediante una llamada a la función [**WMDRMShutdown**](wmdrmshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="79b27-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="79b27-122">Esta función también cierra COM automáticamente.</span><span class="sxs-lookup"><span data-stu-id="79b27-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="79b27-123">En el ejemplo de código siguiente se muestra cómo inicializar y concluir una aplicación que usa las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="79b27-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="79b27-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79b27-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79b27-125">**Introducción**</span><span class="sxs-lookup"><span data-stu-id="79b27-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




