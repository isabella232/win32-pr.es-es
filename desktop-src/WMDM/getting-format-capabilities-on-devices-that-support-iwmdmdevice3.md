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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Obtener capacidades de formato a través de IWMDMDevice3

[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) es el método preferido para pedir a un dispositivo los formatos que admite. En los pasos siguientes se muestra cómo usar este método para consultar sus capacidades de formato en un dispositivo:

1.  La aplicación debe determinar qué formatos admite un dispositivo y cuáles son de interés. Para ello, la aplicación puede solicitar una lista de formatos admitidos por el dispositivo mediante una llamada a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  La aplicación recorre en bucle todos los formatos admitidos y solicita las capacidades de formato de un dispositivo para un formato específico (como WMA o WMV) mediante una llamada a **IWMDMDevice3:: GetFormatCapability** y especificando un formato mediante la enumeración [**\_ FORMATCODE de WMDM**](wmdm-formatcode.md) . Este método recupera una estructura [**de \_ \_ capacidad de formato WMDM**](wmdm-format-capability.md) .
3.  Recorra en bucle todas las estructuras de [**\_ \_ configuración de propiedades de WMDM**](wmdm-prop-config.md) en la estructura de **\_ \_ capacidad del formato WMDM** recuperada. Cada estructura de **\_ \_ configuración** de propiedades de WMDM contiene un grupo de propiedades con valores admitidos que representan una configuración para ese formato. Cada configuración tiene un número de preferencia, donde un número más bajo indica una mayor preferencia por el dispositivo.
4.  Recorra en bucle todas las estructuras de la [**\_ \_ Descripción de propiedades de WMDM**](wmdm-prop-desc.md) en el archivo de **\_ \_ configuración de propiedades de WMDM** recuperado. Cada **\_ \_ DESC** de la Prop. de WMDM contiene una lista de pares de propiedad/valor admitidos.
5.  Recupere los nombres y los valores de las propiedades de la estructura de **\_ \_ Descripción** de la propiedad WMDM. Las propiedades son velocidad de bits, códec y tamaño de marco. Los nombres de propiedad se definen en el archivo de encabezado mswmdm. h. en las [constantes de metadatos](metadata-constants.md), se proporciona una lista de la mayoría de estas constantes. Son posibles tres tipos de valores de propiedad:
    -   Un valor único, la \_ enumeración de WMDM \_ prop \_ \_ (valores válidos \_ ) any, que indica la compatibilidad con los valores de esta propiedad.
    -   Un intervalo de valores, definido por un valor máximo, el valor mínimo y el intervalo.
    -   Una lista de valores discretos.
6.  Borre los valores almacenados. La memoria para estos valores se asigna mediante Windows Media Administrador de dispositivos; el dispositivo es responsable de liberar memoria. Al final de este tema se describe cómo hacerlo.

Al responder a **GetFormatCapability**, un dispositivo puede informar \_ \_ \_ de los valores válidos de la enumeración WMDM \_ para la \_ **capacidad de \_ formato WMDM \_ . configuración de propiedades de WMDM \_ \_ . Descripción de la Prop de WMDM \_ \_ . ValidValuesForm** para notificar la compatibilidad con cualquier valor de velocidad de bits, canales, etc. Sin embargo, debe tratar esta notificación con precaución, ya que los dispositivos a veces pueden notificar la compatibilidad de cualquier valor cuando de hecho no admiten todas las velocidades de bits o tamaños de imagen. Considere la posibilidad de hacer que la aplicación transcodifique archivos de alta velocidad de bits o extremadamente grandes en versiones más pequeñas o menos versiones de uso intensivo de memoria y CPU al enviarlas a dispositivos destinados a reproducir estos archivos.

La siguiente función de C++ muestra cómo solicitar compatibilidad con el formato de dispositivo para un formato específico.


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



**Borrar memoria asignada**

Después de recuperar las capacidades de formato de un dispositivo, la aplicación debe liberar la memoria asignada para contener la descripción. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) y [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) tienen matrices de estructuras simples que se pueden borrar simplemente llamando a **CoTaskMemFree** con la matriz. Sin embargo, **GetFormatCapability** tiene una estructura de datos más compleja con memoria asignada dinámicamente que se debe borrar recorriendo en bucle todos los elementos y liberarlos de forma individual.

En el código de C++ siguiente se muestra cómo una aplicación puede liberar la memoria asignada para una estructura de **\_ \_ capacidad de formato WMDM** .


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



**Consultar todos los formatos admitidos**

Normalmente, una aplicación consulta un determinado formato en un dispositivo, ya que está interesado en enviar un archivo específico al dispositivo. Sin embargo, si desea consultar en una aplicación todos los formatos admitidos, puede llamar a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) y pasar g \_ wszWMDMFormatsSupported para recuperar una lista completa.

Si un dispositivo solo devuelve un elemento, WMDM \_ FORMATCODE \_ undefined, normalmente significa que el dispositivo no admite códigos de formato. La llamada a **GetFormatCapability** con WMDM \_ FORMATCODE \_ indefinido podría recuperar funcionalidades, pero estas propiedades podrían ser bastante genéricas (como el nombre, el tamaño del archivo, la fecha de la última modificación, etc.).

En los pasos siguientes se muestra cómo consultar una lista de todos los formatos admitidos:

1.  Solicite una lista de todos los códigos de formato admitidos llamando a **IWMDMDevice3:: GetProperty** y pasando g \_ wszWMDMFormatsSupported. Esto devuelve un **PROPVARIANT** que contiene una **SAFEARRAY** de formatos admitidos.
2.  Recorra los elementos mediante una llamada a **SafeArrayGetElement**. Cada elemento es una enumeración **\_ FORMATCODE de WMDM** .
3.  Solicite las capacidades de cada formato, liberando la memoria de cada elemento de **\_ \_ capacidad de formato WMDM** una vez que se haya hecho con él.
4.  Borre el **PROPVARIANT** recuperado en el paso 1 mediante una llamada a **PropVariantClear**.

En el siguiente código de ejemplo de C++ se recupera una lista de formatos admitidos para un dispositivo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Detección de capacidades de formato de dispositivo**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




