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
# <a name="retrieving-supported-service-methods"></a>Recuperando métodos de servicio admitidos

Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa. Son específicos de cada tipo de servicio y se representan mediante un GUID único.

Por ejemplo, el servicio contactos define un método **BeginSync** que las aplicaciones llaman para preparar el dispositivo para la sincronización de objetos de contacto y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización.

Las aplicaciones pueden consultar mediante programación los métodos admitidos y acceder a estos métodos y sus atributos mediante la interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .

Los métodos de servicio no deben confundirse con los comandos de WPD. Los comandos de WPD forman parte de la interfaz de controlador de dispositivo (DDI) de WPD estándar y son el mecanismo para la comunicación entre una aplicación de WPD y el controlador. Los comandos están predefinidos, agrupados por categorías, por ejemplo, \_ la categoría de WPD \_ común y se representan mediante una estructura PROPERTYKEY. Para obtener más información, vea el tema [**comandos**](commands.md) .

La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede recuperar los métodos admitidos por un servicio de contactos determinado mediante las interfaces de la tabla siguiente.



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfaz                                                                            | Descripción                                                                                                    |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Se usa para recuperar la interfaz **IPortableDeviceServiceCapabilities** para tener acceso a los métodos de servicio admitidos. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Proporciona acceso a los métodos admitidos, los atributos de método y los parámetros de método.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene la lista de métodos admitidos.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene los atributos de un método y de los parámetros de un método determinado.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Contiene los parámetros de un método determinado.                                                                    |



 

Cuando el usuario elige la opción "5" en la línea de comandos, la aplicación invoca el método **ListSupportedMethods** que se encuentra en el módulo ServiceMethods. cpp.

Tenga en cuenta que antes de recuperar la lista de eventos, la aplicación de ejemplo abre un servicio de contactos en un dispositivo conectado.

En WPD, un método se describe mediante el nombre, los derechos de acceso, los parámetros y los datos relacionados. La aplicación de ejemplo muestra un nombre descriptivo, por ejemplo, "CustomMethod" o un GUID. El nombre del método o el GUID van seguidos de los datos de Access ("lectura/escritura"), el nombre de los formatos asociados y los datos de los parámetros. Estos datos incluyen el nombre del parámetro, el uso, VARTYPE y el formulario.

Cinco métodos en el módulo ServiceMethods. cpp admiten la recuperación de métodos (y datos relacionados) para el servicio de contactos dado: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters**. El método **ListSupportedMethods** recupera un recuento de los métodos admitidos y el identificador GUID para cada uno; a continuación, llama al método **DisplayMethod** . El método **DisplayMethod** llama al método [**IPortableDeviceServiceCapapbilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar las opciones, los parámetros, etc. del método determinado. Después de que **DisplayMethod** recupere los datos del método, representa el nombre (o GUID), las restricciones de acceso, el formato asociado (si existe) y las descripciones de los parámetros. **DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters** son funciones auxiliares que representan sus respectivos campos de datos.

El método **ListSupportedMethods** invoca el método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una interfaz [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Mediante esta interfaz, se recuperan los métodos admitidos llamando al método [**IPortableDeviceServiceCapabilities:: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . El método **GetSupportedMethods** recupera los GUID de cada método admitido por el servicio y copia ese GUID en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

En el código siguiente se usa el método **ListSupportedMethods** .


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



Después de que el método **ListSupportedMethods** recupera el GUID para cada evento admitido por el servicio determinado, invoca el método **DisplayMethod** para recuperar los atributos específicos del método. Estos atributos incluyen: el nombre descriptivo del método, las restricciones de acceso requeridas, los formatos asociados y la lista de parámetros.

El método **DisplayMethod** invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar una colección de atributos para el método especificado. A continuación, llama al método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) para recuperar el nombre del método. **DisplayMethod** llama a [**IPortableDeviceValues:: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) para recuperar el restrctions de acceso. Después, llama a [**IPortableDeviceValues:: GetGuidValue**](iportabledevicevalues-getguidvalue.md) para recuperar cualquier formato asociado. Y, por último, **DisplayMethod** llama a [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar los datos del parámetro. Pasa los datos devueltos por estos métodos a las funciones auxiliares **DisplayMethodAccess**, **DisplayFormat** y **DisplayMethodParameters** , que representan la información del método especificado.

En el código siguiente se usa el método **DisplayMethod** .


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



La función auxiliar **DisplayMethodAccess** recibe un valor DWORD que contiene las opciones de acceso del método. Compara este valor con \_ el comando de WPD \_ Access \_ Read y \_ el comando \_ \_ de acceso de comandos de WPD ReadWrite para determinar el privilegio de acceso del método. Con el resultado, representa una cadena que indica la restricción de acceso para el método especificado.

En el código siguiente se usa la función auxiliar **DisplayMethodAccess** .


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



La función auxiliar **DisplayMethod** recibe un objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) y el GUID del método como parámetros. Con el objeto **IPortableDeviceServiceCapabilities** , invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) para recuperar los atributos de método y representarlos en la ventana de la consola de la aplicación.

La función auxiliar **DisplayMethodParameters** recibe un objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , el GUID del método y un objeto IPortableDeviceKeyCollection que contiene los parámetros del método. Con el objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , invoca el método [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) para recuperar el nombre del parámetro, el uso, VARTYPE y el formulario. Representa esta información en la ventana de la consola de la aplicación.

En el código siguiente se usa la función auxiliar **DisplayMethodParameters** .


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



