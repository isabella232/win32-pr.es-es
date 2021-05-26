---
title: Recuperación de propiedades de objetos WPD
description: Recuperar propiedades de objeto
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c206b6e3afe75144ce10de615657e788d6d1c
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424065"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="d7ffd-103">Recuperación de propiedades de objetos WPD</span><span class="sxs-lookup"><span data-stu-id="d7ffd-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="d7ffd-104">Los servicios suelen contener objetos secundarios que pertenecen a uno de los formatos que admite cada servicio.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="d7ffd-105">Por ejemplo, un servicio Contactos puede admitir varios objetos de contacto con el formato abstracto Contacto.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="d7ffd-106">Cada objeto de contacto se describe mediante propiedades relacionadas (nombre de contacto, número de teléfono, dirección de correo electrónico, entre otras).</span><span class="sxs-lookup"><span data-stu-id="d7ffd-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="d7ffd-107">La aplicación WpdServiceApiSample incluye código que muestra cómo una aplicación puede recuperar las propiedades content-object admitidas por un servicio Contacts determinado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="d7ffd-108">En este ejemplo se usan las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="d7ffd-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="d7ffd-109">Interface</span></span> | <span data-ttu-id="d7ffd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7ffd-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7ffd-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="d7ffd-112">Recupera la interfaz **IPortableDeviceContent2** para acceder a los métodos de servicio admitidos.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="d7ffd-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="d7ffd-114">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="d7ffd-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="d7ffd-116">Recupera los valores de propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="d7ffd-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="d7ffd-118">Contiene los valores de propiedad que se leyeron para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="d7ffd-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="d7ffd-120">Contiene los parámetros de un método determinado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="d7ffd-121">Cuando el usuario elige la opción "7" en la línea de comandos, la aplicación invoca el método **ReadContentProperties** que se encuentra en el módulo ContentProperties.cpp.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="d7ffd-122">Este método recupera las cuatro propiedades siguientes para el objeto de contacto especificado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="d7ffd-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7ffd-123">Property</span></span>                     | <span data-ttu-id="d7ffd-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7ffd-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="d7ffd-125">Device Services PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="d7ffd-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="d7ffd-126">WPD \_ PROPERTYKEY equivalente</span><span class="sxs-lookup"><span data-stu-id="d7ffd-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="d7ffd-127">Identificador de objeto primario</span><span class="sxs-lookup"><span data-stu-id="d7ffd-127">Parent-object identifier</span></span>     | <span data-ttu-id="d7ffd-128">Cadena que especifica el identificador del elemento primario del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="d7ffd-129">PKEY \_ GenericObj \_ ParentID</span><span class="sxs-lookup"><span data-stu-id="d7ffd-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="d7ffd-130">IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7ffd-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="d7ffd-131">Nombre del objeto</span><span class="sxs-lookup"><span data-stu-id="d7ffd-131">Object name</span></span>                  | <span data-ttu-id="d7ffd-132">Cadena que especifica el nombre del objeto especificado</span><span class="sxs-lookup"><span data-stu-id="d7ffd-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="d7ffd-133">PKEY \_ GenericObj \_ Name</span><span class="sxs-lookup"><span data-stu-id="d7ffd-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="d7ffd-134">NOMBRE DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7ffd-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="d7ffd-135">Identificador único persistente</span><span class="sxs-lookup"><span data-stu-id="d7ffd-135">Persistent unique identifier</span></span> | <span data-ttu-id="d7ffd-136">Cadena que especifica un identificador único para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="d7ffd-137">Este identificador es persistente entre sesiones, a diferencia del identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="d7ffd-138">Para los servicios, debe ser una representación de cadena de un GUID.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="d7ffd-139">PKEY \_ GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="d7ffd-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="d7ffd-140">IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7ffd-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="d7ffd-141">Formato de objeto</span><span class="sxs-lookup"><span data-stu-id="d7ffd-141">Object format</span></span>                | <span data-ttu-id="d7ffd-142">Identificador único global (GUID) que especifica el formato del archivo correspondiente a un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="d7ffd-143">PKEY \_ GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="d7ffd-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="d7ffd-144">FORMATO DE OBJETO \_ \_ WPD</span><span class="sxs-lookup"><span data-stu-id="d7ffd-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="d7ffd-145">Id. primario</span><span class="sxs-lookup"><span data-stu-id="d7ffd-145">Parent ID</span></span>
-   <span data-ttu-id="d7ffd-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7ffd-146">Name</span></span>
-   <span data-ttu-id="d7ffd-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="d7ffd-147">PersistentUID</span></span>
-   <span data-ttu-id="d7ffd-148">Formato</span><span class="sxs-lookup"><span data-stu-id="d7ffd-148">Format</span></span>

<span data-ttu-id="d7ffd-149">Tenga en cuenta que antes de recuperar las propiedades de contenido, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="d7ffd-150">El código siguiente para el **método ReadContentProperties** muestra cómo la aplicación usa la interfaz [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar una [**interfaz IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)</span><span class="sxs-lookup"><span data-stu-id="d7ffd-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="d7ffd-151">Al pasar propertykeys de las propiedades solicitadas al método [**IPortableDeviceProperties::GetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **ReadContentProperties** recupera los valores solicitados y, a continuación, los muestra en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="d7ffd-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d7ffd-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7ffd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ffd-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="d7ffd-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="d7ffd-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="d7ffd-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="d7ffd-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



