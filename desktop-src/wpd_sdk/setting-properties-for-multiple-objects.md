---
description: Establecer las propiedades de varios objetos
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Establecer las propiedades de varios objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716661"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="b4fb4-103">Establecer las propiedades de varios objetos</span><span class="sxs-lookup"><span data-stu-id="b4fb4-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="b4fb4-104">Algunos controladores de dispositivos admiten la configuración de propiedades de varios objetos en una única llamada de función, lo que se conoce como una escritura masiva.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="b4fb4-105">La aplicación puede realizar una escritura masiva con las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="b4fb4-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b4fb4-106">Interface</span></span>                                                                                      | <span data-ttu-id="b4fb4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4fb4-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="b4fb4-108">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="b4fb4-109">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="b4fb4-110">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="b4fb4-111">Proporciona acceso a los métodos específicos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="b4fb4-112">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="b4fb4-113">Admite la operación de escritura masiva.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="b4fb4-114">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b4fb4-115">Se utiliza para almacenar los identificadores de objeto para la operación masiva.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="b4fb4-116">**Interfaz IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="b4fb4-117">Se utiliza para identificar las propiedades que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="b4fb4-118">La `WriteContentPropertiesBulk` función del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de escritura masiva.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="b4fb4-119">La primera tarea que se lleva a cabo en este ejemplo es determinar si el controlador especificado admite operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="b4fb4-120">Esto se logra llamando a QueryInterface en un objeto **IPortableDeviceProperties** y comprobando la existencia de **IPortableDevicePropertiesBulk**.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



<span data-ttu-id="b4fb4-121">La siguiente tarea implica la creación de un objeto **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="b4fb4-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="b4fb4-122">Este es el objeto que contiene los valores de propiedad que escribirá el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-122">This is the object that contains the property values that the sample will write.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="b4fb4-123">Después de esto, el ejemplo crea una instancia de la [**interfaz IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="b4fb4-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="b4fb4-124">La aplicación usará los métodos de esta interfaz para realizar el seguimiento del progreso de la operación de escritura masiva asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="b4fb4-125">La siguiente función a la que llama la aplicación de ejemplo es la `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` función auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="b4fb4-126">Esta función enumera de forma recursiva todos los objetos en un dispositivo determinado y devuelve una [**interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene un identificador para cada objeto encontrado.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="b4fb4-127">Esta función se define en el módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



<span data-ttu-id="b4fb4-128">El objeto **IPortableDevicePropVariantCollection** contiene una colección de valores **PROPVARIANT** indizados del mismo VARTYPE.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="b4fb4-129">En este caso, estos valores contienen un identificador de objeto determinado para cada objeto que se encuentra en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="b4fb4-130">Los identificadores de objeto y sus propiedades de nombre respectivas se almacenan en un objeto [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="b4fb4-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="b4fb4-131">Las propiedades de nombre están organizadas de modo que al primer objeto se le asigna una propiedad de nombre de "NewName0", al segundo objeto se le asigna una propiedad de nombre de "NewName1", y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="b4fb4-132">En el siguiente fragmento del ejemplo se muestra cómo se inicializó el objeto **IPortableDeviceValuesCollection** con identificadores de objeto y nuevas cadenas de nombre.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



<span data-ttu-id="b4fb4-133">Una vez que el ejemplo crea el objeto **IPortableDeviceValuesCollection** que contiene los pares de nombre y identificador de objeto, puede comenzar la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="b4fb4-134">La operación de escritura asincrónica comienza cuando el ejemplo llama al método [**IPortableDevicePropertiesBulk:: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="b4fb4-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="b4fb4-135">Este método notifica al controlador que una operación masiva está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="b4fb4-136">Después de esto, el ejemplo llama al método [**IPortableDeviceBulk:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) para empezar a escribir realmente los nuevos valores de nombre.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



<span data-ttu-id="b4fb4-137">Tenga en cuenta que el ejemplo espera un período de tiempo infinitamente largo para que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="b4fb4-138">Si se trata de una aplicación de producción, es necesario modificar el código.</span><span class="sxs-lookup"><span data-stu-id="b4fb4-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4fb4-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4fb4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4fb4-140">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b4fb4-141">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="b4fb4-142">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="b4fb4-143">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="b4fb4-144">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="b4fb4-145">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="b4fb4-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



