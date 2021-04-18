---
description: Recuperando formatos de servicio admitidos
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recuperando formatos de servicio admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716775"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="18f10-103">Recuperando formatos de servicio admitidos</span><span class="sxs-lookup"><span data-stu-id="18f10-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="18f10-104">La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los formatos admitidos por un servicio de contactos determinado llamando a los métodos de las interfaces de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="18f10-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f10-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="18f10-105">Interface</span></span>                                                                            | <span data-ttu-id="18f10-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="18f10-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="18f10-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="18f10-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="18f10-108">Se usa para recuperar la interfaz **IPortableDeviceServiceCapabilities** para tener acceso a los eventos admitidos.</span><span class="sxs-lookup"><span data-stu-id="18f10-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="18f10-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18f10-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="18f10-110">Proporciona acceso a los eventos y atributos de evento admitidos.</span><span class="sxs-lookup"><span data-stu-id="18f10-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="18f10-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="18f10-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="18f10-112">Contiene la lista de formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="18f10-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="18f10-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="18f10-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="18f10-114">Contiene los atributos de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="18f10-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="18f10-115">Cuando el usuario elige la opción "3" en la línea de comandos, la aplicación invoca el método **ListSupportedFormats** que se encuentra en el módulo ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="18f10-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="18f10-116">Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio de contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="18f10-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="18f10-117">En WPD, un formato se describe mediante atributos que especifican el nombre y, opcionalmente, el tipo MIME de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="18f10-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="18f10-118">Estos atributos se definen en el archivo de encabezado thePortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="18f10-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="18f10-119">Para obtener una descripción de los atributos admitidos, consulte el tema [atributos](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="18f10-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="18f10-120">En el caso de la aplicación de ejemplo, si WpdServiceSampleDriver es el único dispositivo instalado, el controlador devuelve dos formatos compatibles para su servicio de contacto: "AbstractContactFormat" y "VCard2Format".</span><span class="sxs-lookup"><span data-stu-id="18f10-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="18f10-121">Estos formatos corresponden al **\_ \_ \_ \_ contacto Abstract del formato de objeto de WPD** y al formato de **\_ objeto WPD \_ \_ VCARD2** atributos encontrados en PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="18f10-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="18f10-122">Dos métodos en el módulo ServiceCapabilities. cpp admiten la recuperación de formatos admitidos para el servicio de contactos: **ListSupportedFormats** y **DisplayFormat**.</span><span class="sxs-lookup"><span data-stu-id="18f10-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="18f10-123">El primero recupera el identificador GUID para cada formato admitido.</span><span class="sxs-lookup"><span data-stu-id="18f10-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="18f10-124">El último convierte este GUID en una cadena descriptiva para el usuario.</span><span class="sxs-lookup"><span data-stu-id="18f10-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="18f10-125">El método **ListSupportedFormats** invoca el método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="18f10-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="18f10-126">Mediante esta interfaz, recupera los formatos admitidos llamando al método [**IPortableDeviceServiceCapabilities:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) .</span><span class="sxs-lookup"><span data-stu-id="18f10-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="18f10-127">El método **GetSupportedFormats** recupera el GUID para cada formato admitido por el servicio y copia ese GUID en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="18f10-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="18f10-128">En el código siguiente se usa el método **ListSupportedFormats** .</span><span class="sxs-lookup"><span data-stu-id="18f10-128">The following code uses the **ListSupportedFormats** method.</span></span>


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="18f10-129">Después de que el método **ListSupportedFormats** recupera el GUID para cada formato admitido por el servicio determinado, invoca el método **DisplayFormat** para mostrar el nombre descriptivo del script para cada formato. por ejemplo, "VCard2".</span><span class="sxs-lookup"><span data-stu-id="18f10-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="18f10-130">El método **DisplayFormat** invoca el método [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) recupera una colección de atributos para el GUID de formato especificado.</span><span class="sxs-lookup"><span data-stu-id="18f10-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="18f10-131">A continuación, llama al método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) y solicita que el controlador devuelva un nombre descriptivo del script para el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="18f10-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="18f10-132">En el código siguiente se usa el método **DisplayFormat** .</span><span class="sxs-lookup"><span data-stu-id="18f10-132">The following code uses the **DisplayFormat** method.</span></span>


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="18f10-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18f10-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18f10-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="18f10-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="18f10-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18f10-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="18f10-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="18f10-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="18f10-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="18f10-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



