---
title: Obtener capacidades de formato a través de IWMDMDevice3
description: Obtener capacidades de formato en los dispositivos que admiten IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- Administrador de dispositivos, funcionalidades del dispositivo
- Guía de programación, funcionalidades del dispositivo
- aplicaciones de escritorio, funcionalidades de dispositivo
- creación de aplicaciones de Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- escribir archivos en dispositivos, funcionalidades del dispositivo
- Método IWMDMDevice3
- Administrador de dispositivos de Windows Media, método IWMDMDevice3
- Administrador de dispositivos, método IWMDMDevice3
- Guía de programación, método IWMDMDevice3
- aplicaciones de escritorio, método IWMDMDevice3
- crear aplicaciones de Windows Media Administrador de dispositivos, método IWMDMDevice3
- escribir archivos en dispositivos, método IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104077166"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="c024b-116">Obtener capacidades de formato a través de IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="c024b-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="c024b-117">[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) es el método preferido para pedir a un dispositivo los formatos que admite.</span><span class="sxs-lookup"><span data-stu-id="c024b-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="c024b-118">En los pasos siguientes se muestra cómo usar este método para consultar sus capacidades de formato en un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="c024b-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="c024b-119">La aplicación debe determinar qué formatos admite un dispositivo y cuáles son de interés.</span><span class="sxs-lookup"><span data-stu-id="c024b-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="c024b-120">Para ello, la aplicación puede solicitar una lista de formatos admitidos por el dispositivo mediante una llamada a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span><span class="sxs-lookup"><span data-stu-id="c024b-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="c024b-121">La aplicación recorre en bucle todos los formatos admitidos y solicita las capacidades de formato de un dispositivo para un formato específico (como WMA o WMV) mediante una llamada a **IWMDMDevice3:: GetFormatCapability** y especificando un formato mediante la enumeración [**\_ FORMATCODE de WMDM**](wmdm-formatcode.md) .</span><span class="sxs-lookup"><span data-stu-id="c024b-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="c024b-122">Este método recupera una estructura [**de \_ \_ capacidad de formato WMDM**](wmdm-format-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="c024b-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="c024b-123">Recorra en bucle todas las estructuras de [**\_ \_ configuración de propiedades de WMDM**](wmdm-prop-config.md) en la estructura de **\_ \_ capacidad del formato WMDM** recuperada.</span><span class="sxs-lookup"><span data-stu-id="c024b-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="c024b-124">Cada estructura de **\_ \_ configuración** de propiedades de WMDM contiene un grupo de propiedades con valores admitidos que representan una configuración para ese formato.</span><span class="sxs-lookup"><span data-stu-id="c024b-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="c024b-125">Cada configuración tiene un número de preferencia, donde un número más bajo indica una mayor preferencia por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c024b-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="c024b-126">Recorra en bucle todas las estructuras de la [**\_ \_ Descripción de propiedades de WMDM**](wmdm-prop-desc.md) en el archivo de **\_ \_ configuración de propiedades de WMDM** recuperado.</span><span class="sxs-lookup"><span data-stu-id="c024b-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="c024b-127">Cada **\_ \_ DESC** de la Prop. de WMDM contiene una lista de pares de propiedad/valor admitidos.</span><span class="sxs-lookup"><span data-stu-id="c024b-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="c024b-128">Recupere los nombres y los valores de las propiedades de la estructura de **\_ \_ Descripción** de la propiedad WMDM.</span><span class="sxs-lookup"><span data-stu-id="c024b-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="c024b-129">Las propiedades son velocidad de bits, códec y tamaño de marco.</span><span class="sxs-lookup"><span data-stu-id="c024b-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="c024b-130">Los nombres de propiedad se definen en el archivo de encabezado mswmdm. h. en las [constantes de metadatos](metadata-constants.md), se proporciona una lista de la mayoría de estas constantes.</span><span class="sxs-lookup"><span data-stu-id="c024b-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="c024b-131">Son posibles tres tipos de valores de propiedad:</span><span class="sxs-lookup"><span data-stu-id="c024b-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="c024b-132">Un valor único, la \_ enumeración de WMDM \_ prop \_ \_ (valores válidos \_ ) any, que indica la compatibilidad con los valores de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c024b-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="c024b-133">Un intervalo de valores, definido por un valor máximo, el valor mínimo y el intervalo.</span><span class="sxs-lookup"><span data-stu-id="c024b-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="c024b-134">Una lista de valores discretos.</span><span class="sxs-lookup"><span data-stu-id="c024b-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="c024b-135">Borre los valores almacenados.</span><span class="sxs-lookup"><span data-stu-id="c024b-135">Clear the stored values.</span></span> <span data-ttu-id="c024b-136">La memoria para estos valores se asigna mediante Windows Media Administrador de dispositivos; el dispositivo es responsable de liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="c024b-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="c024b-137">Al final de este tema se describe cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="c024b-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="c024b-138">Al responder a **GetFormatCapability**, un dispositivo puede informar \_ \_ \_ de los valores válidos de la enumeración WMDM \_ para la \_ **capacidad de \_ formato WMDM \_ . configuración de propiedades de WMDM \_ \_ . Descripción de la Prop de WMDM \_ \_ . ValidValuesForm** para notificar la compatibilidad con cualquier valor de velocidad de bits, canales, etc.</span><span class="sxs-lookup"><span data-stu-id="c024b-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="c024b-139">Sin embargo, debe tratar esta notificación con precaución, ya que los dispositivos a veces pueden notificar la compatibilidad de cualquier valor cuando de hecho no admiten todas las velocidades de bits o tamaños de imagen.</span><span class="sxs-lookup"><span data-stu-id="c024b-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="c024b-140">Considere la posibilidad de hacer que la aplicación transcodifique archivos de alta velocidad de bits o extremadamente grandes en versiones más pequeñas o menos versiones de uso intensivo de memoria y CPU al enviarlas a dispositivos destinados a reproducir estos archivos.</span><span class="sxs-lookup"><span data-stu-id="c024b-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="c024b-141">La siguiente función de C++ muestra cómo solicitar compatibilidad con el formato de dispositivo para un formato específico.</span><span class="sxs-lookup"><span data-stu-id="c024b-141">The following C++ function shows how to request device format support for a specific format.</span></span>


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



<span data-ttu-id="c024b-142">**Borrar memoria asignada**</span><span class="sxs-lookup"><span data-stu-id="c024b-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="c024b-143">Después de recuperar las capacidades de formato de un dispositivo, la aplicación debe liberar la memoria asignada para contener la descripción.</span><span class="sxs-lookup"><span data-stu-id="c024b-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="c024b-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) y [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) tienen matrices de estructuras simples que se pueden borrar simplemente llamando a **CoTaskMemFree** con la matriz.</span><span class="sxs-lookup"><span data-stu-id="c024b-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="c024b-145">Sin embargo, **GetFormatCapability** tiene una estructura de datos más compleja con memoria asignada dinámicamente que se debe borrar recorriendo en bucle todos los elementos y liberarlos de forma individual.</span><span class="sxs-lookup"><span data-stu-id="c024b-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="c024b-146">En el código de C++ siguiente se muestra cómo una aplicación puede liberar la memoria asignada para una estructura de **\_ \_ capacidad de formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="c024b-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



<span data-ttu-id="c024b-147">**Consultar todos los formatos admitidos**</span><span class="sxs-lookup"><span data-stu-id="c024b-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="c024b-148">Normalmente, una aplicación consulta un determinado formato en un dispositivo, ya que está interesado en enviar un archivo específico al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c024b-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="c024b-149">Sin embargo, si desea consultar en una aplicación todos los formatos admitidos, puede llamar a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) y pasar g \_ wszWMDMFormatsSupported para recuperar una lista completa.</span><span class="sxs-lookup"><span data-stu-id="c024b-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="c024b-150">Si un dispositivo solo devuelve un elemento, WMDM \_ FORMATCODE \_ undefined, normalmente significa que el dispositivo no admite códigos de formato.</span><span class="sxs-lookup"><span data-stu-id="c024b-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="c024b-151">La llamada a **GetFormatCapability** con WMDM \_ FORMATCODE \_ indefinido podría recuperar funcionalidades, pero estas propiedades podrían ser bastante genéricas (como el nombre, el tamaño del archivo, la fecha de la última modificación, etc.).</span><span class="sxs-lookup"><span data-stu-id="c024b-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="c024b-152">En los pasos siguientes se muestra cómo consultar una lista de todos los formatos admitidos:</span><span class="sxs-lookup"><span data-stu-id="c024b-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="c024b-153">Solicite una lista de todos los códigos de formato admitidos llamando a **IWMDMDevice3:: GetProperty** y pasando g \_ wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="c024b-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="c024b-154">Esto devuelve un **PROPVARIANT** que contiene una **SAFEARRAY** de formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="c024b-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="c024b-155">Recorra los elementos mediante una llamada a **SafeArrayGetElement**.</span><span class="sxs-lookup"><span data-stu-id="c024b-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="c024b-156">Cada elemento es una enumeración **\_ FORMATCODE de WMDM** .</span><span class="sxs-lookup"><span data-stu-id="c024b-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="c024b-157">Solicite las capacidades de cada formato, liberando la memoria de cada elemento de **\_ \_ capacidad de formato WMDM** una vez que se haya hecho con él.</span><span class="sxs-lookup"><span data-stu-id="c024b-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="c024b-158">Borre el **PROPVARIANT** recuperado en el paso 1 mediante una llamada a **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="c024b-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="c024b-159">En el siguiente código de ejemplo de C++ se recupera una lista de formatos admitidos para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c024b-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c024b-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c024b-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c024b-161">**Detección de capacidades de formato de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="c024b-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




