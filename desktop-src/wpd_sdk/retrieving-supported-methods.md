---
description: Recuperando métodos de servicio admitidos
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Recuperando métodos de servicio admitidos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911121"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="d076b-103">Recuperando métodos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="d076b-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="d076b-104">Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa.</span><span class="sxs-lookup"><span data-stu-id="d076b-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="d076b-105">Son específicos de cada tipo de servicio y se representan mediante un GUID único.</span><span class="sxs-lookup"><span data-stu-id="d076b-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="d076b-106">Por ejemplo, el servicio contactos define un método **BeginSync** que las aplicaciones llaman para preparar el dispositivo para la sincronización de objetos de contacto y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d076b-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="d076b-107">Las aplicaciones pueden consultar mediante programación los métodos admitidos y acceder a estos métodos y sus atributos mediante la interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="d076b-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="d076b-108">Los métodos de servicio no deben confundirse con los comandos de WPD.</span><span class="sxs-lookup"><span data-stu-id="d076b-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="d076b-109">Los comandos de WPD forman parte de la interfaz de controlador de dispositivo (DDI) de WPD estándar y son el mecanismo para la comunicación entre una aplicación de WPD y el controlador.</span><span class="sxs-lookup"><span data-stu-id="d076b-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="d076b-110">Los comandos están predefinidos, agrupados por categorías, por ejemplo, \_ la categoría de WPD \_ común y se representan mediante una estructura PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="d076b-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="d076b-111">Para obtener más información, vea el tema [**comandos**](commands.md) .</span><span class="sxs-lookup"><span data-stu-id="d076b-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="d076b-112">La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los métodos admitidos por un servicio de contactos determinado mediante las interfaces de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d076b-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d076b-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="d076b-113">Interface</span></span>                                                                            | <span data-ttu-id="d076b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d076b-114">Description</span></span>                                                                                                    |
| [<span data-ttu-id="d076b-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d076b-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="d076b-116">Se usa para recuperar la interfaz **IPortableDeviceServiceCapabilities** para tener acceso a los métodos de servicio admitidos.</span><span class="sxs-lookup"><span data-stu-id="d076b-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="d076b-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d076b-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="d076b-118">Proporciona acceso a los métodos admitidos, los atributos de método y los parámetros de método.</span><span class="sxs-lookup"><span data-stu-id="d076b-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="d076b-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="d076b-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="d076b-120">Contiene la lista de métodos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d076b-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="d076b-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d076b-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="d076b-122">Contiene los atributos de un método y de los parámetros de un método determinado.</span><span class="sxs-lookup"><span data-stu-id="d076b-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="d076b-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d076b-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="d076b-124">Contiene los parámetros de un método determinado.</span><span class="sxs-lookup"><span data-stu-id="d076b-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="d076b-125">Cuando el usuario elige la opción "5" en la línea de comandos, la aplicación invoca el método **ListSupportedMethods** que se encuentra en el módulo ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="d076b-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="d076b-126">Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio de contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="d076b-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="d076b-127">En WPD, un método se describe mediante el nombre, los derechos de acceso, los parámetros y los datos relacionados.</span><span class="sxs-lookup"><span data-stu-id="d076b-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="d076b-128">La aplicación de ejemplo muestra un nombre descriptivo, por ejemplo, "CustomMethod" o un GUID.</span><span class="sxs-lookup"><span data-stu-id="d076b-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="d076b-129">El nombre del método o el GUID van seguidos de los datos de Access ("lectura/escritura"), el nombre de los formatos asociados y los datos de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="d076b-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="d076b-130">Estos datos incluyen el nombre del parámetro, el uso, VARTYPE y el formulario.</span><span class="sxs-lookup"><span data-stu-id="d076b-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="d076b-131">Cinco métodos en el módulo ServiceMethods. cpp admiten la recuperación de métodos (y datos relacionados) para el servicio de contactos dado: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="d076b-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="d076b-132">El método **ListSupportedMethods** recupera un recuento de los métodos admitidos y el identificador GUID para cada uno; a continuación, llama al método **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="d076b-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="d076b-133">El método **DisplayMethod** llama al método [**IPortableDeviceServiceCapapbilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar las opciones, los parámetros, etc. del método determinado.</span><span class="sxs-lookup"><span data-stu-id="d076b-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="d076b-134">Después de que **DisplayMethod** recupere los datos del método, representa el nombre (o GUID), las restricciones de acceso, el formato asociado (si existe) y las descripciones de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="d076b-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="d076b-135">**DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters** son funciones auxiliares que representan sus respectivos campos de datos.</span><span class="sxs-lookup"><span data-stu-id="d076b-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="d076b-136">El método **ListSupportedMethods** invoca el método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="d076b-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="d076b-137">Mediante esta interfaz, se recuperan los métodos admitidos llamando al método [**IPortableDeviceServiceCapabilities:: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="d076b-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="d076b-138">El método **GetSupportedMethods** recupera los GUID de cada método admitido por el servicio y copia ese GUID en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d076b-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="d076b-139">En el código siguiente se usa el método **ListSupportedMethods** .</span><span class="sxs-lookup"><span data-stu-id="d076b-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="d076b-140">Después de que el método **ListSupportedMethods** recupera el GUID para cada evento admitido por el servicio determinado, invoca el método **DisplayMethod** para recuperar los atributos específicos del método.</span><span class="sxs-lookup"><span data-stu-id="d076b-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="d076b-141">Estos atributos incluyen: el nombre descriptivo del método, las restricciones de acceso requeridas, los formatos asociados y la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="d076b-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="d076b-142">El método **DisplayMethod** invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar una colección de atributos para el método especificado.</span><span class="sxs-lookup"><span data-stu-id="d076b-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="d076b-143">A continuación, llama al método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) para recuperar el nombre del método.</span><span class="sxs-lookup"><span data-stu-id="d076b-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="d076b-144">**DisplayMethod** llama a [**IPortableDeviceValues:: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) para recuperar el restrctions de acceso.</span><span class="sxs-lookup"><span data-stu-id="d076b-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="d076b-145">Después, llama a [**IPortableDeviceValues:: GetGuidValue**](iportabledevicevalues-getguidvalue.md) para recuperar cualquier formato asociado.</span><span class="sxs-lookup"><span data-stu-id="d076b-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="d076b-146">Y, por último, **DisplayMethod** llama a [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar los datos del parámetro.</span><span class="sxs-lookup"><span data-stu-id="d076b-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="d076b-147">Pasa los datos devueltos por estos métodos a las funciones auxiliares **DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters** , que representan la información del método especificado.</span><span class="sxs-lookup"><span data-stu-id="d076b-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="d076b-148">En el código siguiente se usa el método **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="d076b-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="d076b-149">La función auxiliar **DisplayMethodAccess** recibe un valor DWORD que contiene las opciones de acceso del método.</span><span class="sxs-lookup"><span data-stu-id="d076b-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="d076b-150">Compara este valor con \_ el comando de WPD \_ Access \_ Read y \_ el comando \_ \_ de acceso de comandos de WPD ReadWrite para determinar el privilegio de acceso del método.</span><span class="sxs-lookup"><span data-stu-id="d076b-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="d076b-151">Con el resultado, representa una cadena que indica la restricción de acceso para el método especificado.</span><span class="sxs-lookup"><span data-stu-id="d076b-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="d076b-152">En el código siguiente se usa la función auxiliar **DisplayMethodAccess** .</span><span class="sxs-lookup"><span data-stu-id="d076b-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="d076b-153">La función auxiliar **DisplayMethod** recibe un objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) y el GUID del método como parámetros.</span><span class="sxs-lookup"><span data-stu-id="d076b-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="d076b-154">Con el objeto **IPortableDeviceServiceCapabilities** , invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) para recuperar los atributos de método y representarlos en la ventana de la consola de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d076b-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="d076b-155">La función auxiliar **DisplayMethodParameters** recibe un objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , el GUID del método y un objeto IPortableDeviceKeyCollection que contiene los parámetros del método.</span><span class="sxs-lookup"><span data-stu-id="d076b-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="d076b-156">Con el objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) para recuperar el nombre del parámetro, el uso, VARTYPE y el formulario.</span><span class="sxs-lookup"><span data-stu-id="d076b-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="d076b-157">Representa esta información en la ventana de la consola de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d076b-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="d076b-158">En el código siguiente se usa la función auxiliar **DisplayMethodParameters** .</span><span class="sxs-lookup"><span data-stu-id="d076b-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d076b-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d076b-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d076b-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d076b-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="d076b-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d076b-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d076b-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d076b-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="d076b-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d076b-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d076b-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="d076b-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



