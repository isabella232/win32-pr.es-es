---
description: Establecer propiedades para un solo objeto
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Establecer propiedades para un solo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717060"
---
# <a name="setting-properties-for-a-single-object"></a><span data-ttu-id="36e84-103">Establecer propiedades para un solo objeto</span><span class="sxs-lookup"><span data-stu-id="36e84-103">Setting Properties for a Single Object</span></span>

<span data-ttu-id="36e84-104">Una vez que la aplicación recupera un identificador de objeto (vea el tema [enumerar contenido](enumerating-content.md) ) de un objeto determinado, puede establecer las propiedades de ese objeto llamando a los métodos de las interfaces que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="36e84-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can set properties for that object by calling methods in the interfaces described in the following table.</span></span>



| <span data-ttu-id="36e84-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="36e84-105">Interface</span></span>                                                                | <span data-ttu-id="36e84-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="36e84-106">Description</span></span>                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36e84-107">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="36e84-107">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="36e84-108">Se utiliza para determinar si se puede escribir una propiedad determinada y enviar la operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="36e84-108">Used to determine whether a given property can be written and to send the write operation.</span></span>                                                                  |
| [<span data-ttu-id="36e84-109">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="36e84-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="36e84-110">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="36e84-110">Provides access to the content-specific methods.</span></span>                                                                                                            |
| [<span data-ttu-id="36e84-111">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="36e84-111">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="36e84-112">Se utiliza para contener los valores que se van a escribir, determinar los resultados de la operación de escritura y recuperar los atributos de las propiedades (al determinar la capacidad de escritura).</span><span class="sxs-lookup"><span data-stu-id="36e84-112">Used to hold the values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="36e84-113">Las aplicaciones establecen las propiedades de un objeto creando primero un contenedor de propiedades que especifica los nuevos valores mediante la [**interfaz IPortableDeviceValues**](iportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="36e84-113">Applications set properties on an object by first creating a property bag that specifies the new values using the [**IPortableDeviceValues interface**](iportabledevicevalues.md).</span></span> <span data-ttu-id="36e84-114">Una vez que se crea el contenedor de propiedades, una aplicación establece esas propiedades mediante una llamada al método [**IPortableDeviceProperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) .</span><span class="sxs-lookup"><span data-stu-id="36e84-114">Once the property bag is created, an application sets those properties by calling the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) method.</span></span>

<span data-ttu-id="36e84-115">La `WriteContentProperties` función del módulo ContentProperties. cpp de la aplicación de ejemplo muestra cómo una aplicación puede establecer una nueva propiedad de nombre de objeto para un objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="36e84-115">The `WriteContentProperties` function in the sample application's ContentProperties.cpp module demonstrates how an application could set a new object-name property for a selected object.</span></span>

<span data-ttu-id="36e84-116">La primera tarea que se realiza mediante la `WriteContentProperties` función es pedir al usuario que escriba un identificador de objeto para el objeto para el que la aplicación escribirá el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="36e84-116">The first task accomplished by the `WriteContentProperties` function is to prompt the user to enter an object identifier for the object that the application will write the new name for.</span></span>


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



<span data-ttu-id="36e84-117">Después, la aplicación recupera el \_ atributo de propiedad WPD \_ \_ puede \_ escribir el valor de la \_ propiedad del nombre de objeto WPD \_ para determinar si se puede escribir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="36e84-117">After this, the application retrieves the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value for the WPD\_OBJECT\_NAME property to determine whether the property can be written.</span></span> <span data-ttu-id="36e84-118">(Tenga en cuenta que la aplicación podría establecer cualquier propiedad para la que el WPD \_ El \_ atributo de propiedad \_ puede \_ escribir el valor es true).</span><span class="sxs-lookup"><span data-stu-id="36e84-118">(Note that your application could set any property for which the WPD\_PROPERTY\_ATTRIBUTE\_CAN\_WRITE value is true.)</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



<span data-ttu-id="36e84-119">El siguiente paso es preguntar al usuario sobre la nueva cadena de nombre.</span><span class="sxs-lookup"><span data-stu-id="36e84-119">The next step is to prompt the user for the new name string.</span></span> <span data-ttu-id="36e84-120">(Tenga en cuenta que la llamada al método [**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) simplemente crea el contenedor de propiedades; todavía no se ha escrito la propiedad real).</span><span class="sxs-lookup"><span data-stu-id="36e84-120">(Note that the call to the [**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md) method merely creates the property bag; the actual property has not been written yet.)</span></span>


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



<span data-ttu-id="36e84-121">Por último, el nuevo valor, especificado por el usuario, se aplica al objeto.</span><span class="sxs-lookup"><span data-stu-id="36e84-121">Finally, the new value, specified by the user, is applied to the object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="36e84-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36e84-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36e84-123">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="36e84-123">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="36e84-124">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="36e84-124">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="36e84-125">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="36e84-125">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="36e84-126">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="36e84-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="36e84-127">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="36e84-127">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="36e84-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="36e84-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="36e84-129">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="36e84-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



