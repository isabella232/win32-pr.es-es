---
description: Invocación de los métodos de servicio
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Invocación de los métodos de servicio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424205"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="a1f6c-103">Invocación de los métodos de servicio</span><span class="sxs-lookup"><span data-stu-id="a1f6c-103">Invoking Service Methods</span></span>

<span data-ttu-id="a1f6c-104">La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede invocar los métodos admitidos por un servicio Contacts determinado de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="a1f6c-105">En este ejemplo se usan las interfaces siguientes</span><span class="sxs-lookup"><span data-stu-id="a1f6c-105">This sample uses the following interfaces</span></span>



| <span data-ttu-id="a1f6c-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="a1f6c-106">Interface</span></span>    | <span data-ttu-id="a1f6c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1f6c-107">Description</span></span>    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1f6c-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="a1f6c-109">Se usa para recuperar la **interfaz IPortableDeviceServiceMethods** para invocar métodos en un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="a1f6c-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="a1f6c-111">Se usa para invocar un método de servicio.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="a1f6c-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="a1f6c-113">Se usa para contener los parámetros del método saliente y los resultados del método entrante.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="a1f6c-114">Puede ser **NULL si** el método no requiere parámetros ni devuelve ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="a1f6c-115">Cuando el usuario elige la opción "9" en la línea de comandos, la aplicación invoca el método **InvokeMethods** que se encuentra en el módulo ServiceMethods.cpp.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="a1f6c-116">Tenga en cuenta que antes de invocar los métodos, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="a1f6c-117">Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="a1f6c-118">Son únicos para cada tipo de servicio y se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="a1f6c-119">Por ejemplo, el servicio Contacts define un método **BeginSync** al que llaman las aplicaciones para preparar el dispositivo para sincronizar objetos Contact y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="a1f6c-120">Las aplicaciones ejecutan un método mediante una [**llamada a IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="a1f6c-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="a1f6c-121">Los métodos de servicio no deben confundirse con los comandos de WPD.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="a1f6c-122">Los comandos WPD forman parte de la interfaz de controlador de dispositivos (DDI) WPD estándar y son el mecanismo para la comunicación entre una aplicación WPD y el controlador.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="a1f6c-123">Los comandos están predefinidos, agrupados por categorías, por ejemplo, **WPD \_ CATEGORY \_ COMMON** y se representan mediante una **estructura PROPERTYKEY.**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="a1f6c-124">Una aplicación envía comandos al controlador de dispositivo mediante una llamada [**a IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="a1f6c-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="a1f6c-125">Para obtener más información, vea el tema Comandos.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="a1f6c-126">El **método InvokeMethods** invoca el método [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una [**interfaz IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)</span><span class="sxs-lookup"><span data-stu-id="a1f6c-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="a1f6c-127">Con esta interfaz, invoca los métodos **BeginSync** y **EndSync** llamando al método [**IPortableDeviceServiceMethods::Invoke.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods)</span><span class="sxs-lookup"><span data-stu-id="a1f6c-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="a1f6c-128">Cada vez que llama a **Invoke**, la aplicación proporciona el REFGUID para el método que se invoca.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="a1f6c-129">En el código siguiente se usa **el método InvokeMethods.**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a1f6c-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1f6c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1f6c-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="a1f6c-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="a1f6c-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="a1f6c-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="a1f6c-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



