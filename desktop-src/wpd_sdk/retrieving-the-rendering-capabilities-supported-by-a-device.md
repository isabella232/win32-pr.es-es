---
description: Recuperación de las capacidades de representación admitidas por un dispositivo
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Recuperación de las capacidades de representación admitidas por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523f1f9bbcaefe1c502c7c74252582fddcadad4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361467"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a><span data-ttu-id="f5a97-103">Recuperación de las capacidades de representación admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="f5a97-103">Retrieving the Rendering Capabilities Supported by a Device</span></span>

<span data-ttu-id="f5a97-104">Los dispositivos portátiles de Windows que admiten la categoría funcional información de representación ( \_ información de representación de categoría funcional de WPD \_ \_ \_ ) devolverán información de representación cuando se realicen consultas.</span><span class="sxs-lookup"><span data-stu-id="f5a97-104">Windows Portable Devices that support the rendering information functional category (WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION) will return rendering information when queried.</span></span> <span data-ttu-id="f5a97-105">La información de representación describe los requisitos y las restricciones impuestas a las aplicaciones que intentan escribir contenido en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5a97-105">The rendering information describes requirements and restrictions imposed on applications that attempt to write content to a device.</span></span>

<span data-ttu-id="f5a97-106">La función ListRenderingCapabilityInformation, la función auxiliar SupportsFunctionalCategory y la función auxiliar ReadProfileInformationProperties del módulo DeviceCapabilities. cpp muestran la recuperación de las capacidades de representación de un dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-106">The ListRenderingCapabilityInformation function, the SupportsFunctionalCategory helper function, and the ReadProfileInformationProperties helper function in the DeviceCapabilities.cpp module demonstrate the retrieval of rendering capabilities for a selected device.</span></span>

<span data-ttu-id="f5a97-107">La aplicación puede recuperar las capacidades de representación admitidas por un dispositivo mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5a97-107">Your application can retrieve the rendering capabilities supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="f5a97-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f5a97-108">Interface</span></span>                                                                                      | <span data-ttu-id="f5a97-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5a97-109">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="f5a97-110">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f5a97-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="f5a97-111">Proporciona acceso a la interfaz IPortableDeviceProperties.</span><span class="sxs-lookup"><span data-stu-id="f5a97-111">Provides access to the IPortableDeviceProperties interface.</span></span> |
| [<span data-ttu-id="f5a97-112">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="f5a97-112">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="f5a97-113">Proporciona acceso a los métodos específicos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f5a97-113">Provides access to the property-specific methods.</span></span>           |
| [<span data-ttu-id="f5a97-114">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-114">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="f5a97-115">Se usa para almacenar las claves de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-115">Used to store the property keys for the given profile.</span></span>      |
| [<span data-ttu-id="f5a97-116">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f5a97-116">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="f5a97-117">Se usa para almacenar los valores de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-117">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="f5a97-118">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f5a97-118">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="f5a97-119">Se usa para almacenar los valores de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-119">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="f5a97-120">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-120">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f5a97-121">Se usa para almacenar los valores de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-121">Used store the property values for the given profile.</span></span>       |
| [<span data-ttu-id="f5a97-122">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-122">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="f5a97-123">Se usa para almacenar los valores de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="f5a97-123">Used store the property values for the given profile.</span></span>       |



 

<span data-ttu-id="f5a97-124">Una de las primeras tareas que se llevan a cabo mediante la aplicación de ejemplo es determinar si el dispositivo seleccionado es capaz de enumerar las capacidades de representación.</span><span class="sxs-lookup"><span data-stu-id="f5a97-124">One of the first tasks accomplished by the sample application is to determine whether the selected device is capable of listing rendering capabilities.</span></span> <span data-ttu-id="f5a97-125">La función auxiliar SupportsFunctionalCategory determina si este es el caso llamando a la función auxiliar ListRenderingCapabilityInformation y pasando la información de \_ representación de la categoría funcional de WPD \_ \_ \_ como segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="f5a97-125">The SupportsFunctionalCategory helper function determines whether this is the case by calling the ListRenderingCapabilityInformation helper function and passing WPD\_FUNCTIONAL\_CATEGORY\_RENDERING\_INFORMATION as the second argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



<span data-ttu-id="f5a97-126">Si el dispositivo es capaz de enumerar las capacidades de representación, el paso siguiente implica recuperar un objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) e invocar el método [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) para recuperar un identificador de objeto para el objeto de información de representación.</span><span class="sxs-lookup"><span data-stu-id="f5a97-126">If the device is capable of listing rendering capabilities, the next step entails retrieving an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object and invoking the [**GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method to retrieve an object identifier for the rendering-information object.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="f5a97-127">El siguiente paso consiste en almacenar el identificador de objeto de información de representación que se acaba de recuperar en una variable de cadena (strRenderingInfoObjectID) y, a continuación, llamar a la función auxiliar ReadProfileInformationProperties.</span><span class="sxs-lookup"><span data-stu-id="f5a97-127">The next step is to store the rendering-information object identifier that was just retrieved in a string variable (strRenderingInfoObjectID), and then to call the ReadProfileInformationProperties helper function.</span></span> <span data-ttu-id="f5a97-128">(La variable, strRenderingInfoObjectID, se pasa como el segundo argumento a la función auxiliar).</span><span class="sxs-lookup"><span data-stu-id="f5a97-128">(The variable, strRenderingInfoObjectID, is passed as the second argument to the helper function.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



<span data-ttu-id="f5a97-129">Una de las primeras tareas que realiza la función auxiliar es recuperar un objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que se usará para tener acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="f5a97-129">One of the first tasks accomplished by the helper function is to retrieve an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to access the content-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="f5a97-130">A continuación, la función auxiliar recupera un objeto [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) , que se usará para tener acceso a los métodos específicos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f5a97-130">Next, the helper function retrieves an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) object, which it will use to access the property-specific methods.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="f5a97-131">El siguiente paso consiste en crear un objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) en el que se almacenan las claves de propiedad de la información de representación.</span><span class="sxs-lookup"><span data-stu-id="f5a97-131">The next step is to create an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object into which the property keys for the rendering information are stored.</span></span> <span data-ttu-id="f5a97-132">Una vez creado el objeto, se invoca el método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) para agregar las claves necesarias.</span><span class="sxs-lookup"><span data-stu-id="f5a97-132">Once the object is created, the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method is invoked to add the necessary keys.</span></span> <span data-ttu-id="f5a97-133">(Es necesario agregar estas claves para que se puedan recuperar los perfiles de representación correspondientes en los pasos siguientes).</span><span class="sxs-lookup"><span data-stu-id="f5a97-133">(It is necessary to add these keys so that the corresponding rendering profiles can be retrieved in the subsequent steps.)</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="f5a97-134">El siguiente paso consiste en recuperar los valores de propiedad del controlador de dispositivo mediante una llamada al método [**IPortableDeviceProperties:: getValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) .</span><span class="sxs-lookup"><span data-stu-id="f5a97-134">The next step is to retrieve the property values from the device driver by calling the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



<span data-ttu-id="f5a97-135">El paso siguiente recupera el perfil de información de representación y lo almacena en el argumento ppRenderingInfoProfiles.</span><span class="sxs-lookup"><span data-stu-id="f5a97-135">The next step retrieves the rendering-information profile and stores it in the ppRenderingInfoProfiles argument.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



<span data-ttu-id="f5a97-136">Después de que la función auxiliar Lea las \_ propiedades de perfiles de información de representación de WPD \_ \_ , se mostrarán los perfiles de representación.</span><span class="sxs-lookup"><span data-stu-id="f5a97-136">After the helper function reads the WPD\_RENDERING\_INFORMATION\_PROFILES properties, the rendering profiles are displayed.</span></span> <span data-ttu-id="f5a97-137">Estos perfiles se muestran mediante la función auxiliar DisplayRenderingProfile.</span><span class="sxs-lookup"><span data-stu-id="f5a97-137">These profiles are displayed by the DisplayRenderingProfile helper function.</span></span>


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



<span data-ttu-id="f5a97-138">Tenga en cuenta que, como los perfiles de representación son estáticos, la aplicación puede optar por leer los perfiles y almacenarlos localmente (en lugar de acceder al dispositivo cada vez que se necesitan los datos).</span><span class="sxs-lookup"><span data-stu-id="f5a97-138">Note that since the rendering profiles are static, your application may choose to read the profiles and store them locally (instead of accessing the device each time the data is needed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5a97-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5a97-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5a97-140">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="f5a97-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f5a97-141">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f5a97-141">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="f5a97-142">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="f5a97-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="f5a97-143">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="f5a97-144">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="f5a97-145">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a97-145">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> <dt>

[<span data-ttu-id="f5a97-146">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="f5a97-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



