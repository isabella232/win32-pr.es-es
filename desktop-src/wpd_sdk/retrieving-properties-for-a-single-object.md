---
description: Recuperación de propiedades para un solo objeto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recuperación de propiedades para un solo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716574"
---
# <a name="retrieving-properties-for-a-single-object"></a><span data-ttu-id="0de64-103">Recuperación de propiedades para un solo objeto</span><span class="sxs-lookup"><span data-stu-id="0de64-103">Retrieving Properties for a Single Object</span></span>

<span data-ttu-id="0de64-104">Una vez que la aplicación recupera un identificador de objeto (vea el tema [enumerar contenido](enumerating-content.md) ) de un objeto determinado, puede recuperar información descriptiva sobre ese objeto llamando a métodos en la [**interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) y la [**interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="0de64-104">After your application retrieves an object identifier (see the [Enumerating Content](enumerating-content.md) topic) for a given object, it can retrieve descriptive information about that object by calling methods in the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) and the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md).</span></span>

<span data-ttu-id="0de64-105">El método [**IPortableDeviceProperties:: getValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera una lista de propiedades especificadas para un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="0de64-105">The [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method retrieves a list of specified properties for a given object.</span></span> <span data-ttu-id="0de64-106">(La aplicación también podría llamar al método GetValues y especificar un valor **null** para el parámetro pKeys para recuperar todas las propiedades de un objeto determinado; sin embargo, el rendimiento de este método puede ser significativamente más lento al recuperar todas las propiedades).</span><span class="sxs-lookup"><span data-stu-id="0de64-106">(Your application could also call the GetValues method and specify a **NULL** value for the pKeys parameter to retrieve all properties for a given object; however, the performance of this method may be significantly slower when retrieving all properties.)</span></span>

<span data-ttu-id="0de64-107">Sin embargo, antes de que la aplicación llame a GetValues, debe identificar las propiedades que se van a recuperar estableciendo las claves correspondientes en un [**objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).</span><span class="sxs-lookup"><span data-stu-id="0de64-107">Before your application calls GetValues, however, it needs to identify the properties to retrieve by setting corresponding keys in an [**IPortableDeviceKeyCollection object**](iportabledevicekeycollection.md).</span></span> <span data-ttu-id="0de64-108">La aplicación identificará las propiedades de interés llamando al método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) y proporcionando un valor PROPERTYKEY que identifique cada propiedad que recuperará.</span><span class="sxs-lookup"><span data-stu-id="0de64-108">Your application will identify the properties of interest by calling the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method and supplying a PROPERTYKEY value that identifies each property that it will retrieve.</span></span>

<span data-ttu-id="0de64-109">La función ReadContentProperties del módulo ContentProperties. cpp de la aplicación de ejemplo muestra cómo se recuperaron las cinco propiedades de un objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0de64-109">The ReadContentProperties function in the ContentProperties.cpp module of the sample application demonstrates how the five properties were retrieved for a selected object.</span></span> <span data-ttu-id="0de64-110">En la tabla siguiente se describe cada una de estas propiedades y su valor REFPROPERTYKEY correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0de64-110">The following table describes each of these properties and their corresponding REFPROPERTYKEY value.</span></span>



| <span data-ttu-id="0de64-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0de64-111">Property</span></span>                     | <span data-ttu-id="0de64-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0de64-112">Description</span></span>                                                                                                                                      | <span data-ttu-id="0de64-113">PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="0de64-113">PROPERTYKEY</span></span>                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="0de64-114">Identificador de objeto primario</span><span class="sxs-lookup"><span data-stu-id="0de64-114">Parent-object identifier</span></span>     | <span data-ttu-id="0de64-115">Cadena que especifica el identificador del elemento primario del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0de64-115">A string that specifies the identifier for the given object's parent.</span></span>                                                                            | <span data-ttu-id="0de64-116">\_ \_ ID. primario del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="0de64-116">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="0de64-117">Nombre del objeto</span><span class="sxs-lookup"><span data-stu-id="0de64-117">Object name</span></span>                  | <span data-ttu-id="0de64-118">Cadena que especifica el nombre del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0de64-118">A string that specifies the name of the given object.</span></span>                                                                                            | <span data-ttu-id="0de64-119">\_nombre del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="0de64-119">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="0de64-120">Identificador único persistente</span><span class="sxs-lookup"><span data-stu-id="0de64-120">Persistent unique identifier</span></span> | <span data-ttu-id="0de64-121">Cadena que especifica un identificador único para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0de64-121">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="0de64-122">(Este identificador se mantiene en todas las sesiones, a diferencia del identificador de objeto).</span><span class="sxs-lookup"><span data-stu-id="0de64-122">(This identifier is persistent across sessions, unlike the object identifier.)</span></span> | <span data-ttu-id="0de64-123">\_ \_ \_ identificador único persistente del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="0de64-123">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="0de64-124">Formato de objeto</span><span class="sxs-lookup"><span data-stu-id="0de64-124">Object format</span></span>                | <span data-ttu-id="0de64-125">Identificador único global (GUID) que especifica el formato del archivo correspondiente a un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="0de64-125">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object.</span></span>                                       | <span data-ttu-id="0de64-126">\_formato de objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="0de64-126">WPD\_OBJECT\_FORMAT</span></span>                 |
| <span data-ttu-id="0de64-127">Tipo de contenido del objeto</span><span class="sxs-lookup"><span data-stu-id="0de64-127">Object content type</span></span>          | <span data-ttu-id="0de64-128">GUID que especifica el tipo de contenido asociado a un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="0de64-128">A GUID that specifies the type of content associated with a given object.</span></span>                                                                        | <span data-ttu-id="0de64-129">\_tipo de \_ contenido del objeto WPD \_</span><span class="sxs-lookup"><span data-stu-id="0de64-129">WPD\_OBJECT\_CONTENT\_TYPE</span></span>          |



 

<span data-ttu-id="0de64-130">En el siguiente fragmento de la función ReadContentProperties se muestra cómo la aplicación de ejemplo usó la [**interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) y el método [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) para identificar las propiedades que recuperaría.</span><span class="sxs-lookup"><span data-stu-id="0de64-130">The following excerpt from the ReadContentProperties function demonstrates how the sample application used the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and the [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) method to identify the properties it would retrieve.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



<span data-ttu-id="0de64-131">Una vez que la aplicación de ejemplo establece las claves apropiadas, llamó al método [**IPortableDeviceProperties:: getValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) para recuperar los valores especificados para el objeto dado.</span><span class="sxs-lookup"><span data-stu-id="0de64-131">Once the sample application set the appropriate keys, it called the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method to retrieve the specified values for the given object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0de64-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0de64-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0de64-133">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="0de64-133">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="0de64-134">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="0de64-134">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="0de64-135">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0de64-135">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="0de64-136">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="0de64-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



