---
description: Recuperar propiedades de varios objetos
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recuperar propiedades de varios objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716777"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="c788e-103">Recuperar propiedades de varios objetos</span><span class="sxs-lookup"><span data-stu-id="c788e-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="c788e-104">Algunos controladores de dispositivos admiten la recuperación de propiedades de varios objetos en una única llamada de función; Esto se conoce como recuperación masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="c788e-105">Hay dos tipos de operaciones de recuperación masiva: el primer tipo recupera las propiedades de una lista de objetos y el segundo tipo recupera las propiedades de todos los objetos de un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="c788e-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="c788e-106">En el ejemplo descrito en esta sección se muestra el anterior.</span><span class="sxs-lookup"><span data-stu-id="c788e-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="c788e-107">La aplicación puede realizar una recuperación masiva con las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c788e-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="c788e-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c788e-108">Interface</span></span>                                                                                      | <span data-ttu-id="c788e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c788e-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c788e-110">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="c788e-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="c788e-111">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="c788e-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="c788e-112">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="c788e-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="c788e-113">Se utiliza para identificar las propiedades que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c788e-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="c788e-114">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="c788e-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="c788e-115">Se utiliza para determinar si un controlador determinado admite operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="c788e-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="c788e-116">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="c788e-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="c788e-117">Admite la operación de recuperación masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="c788e-118">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c788e-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="c788e-119">Se utiliza para almacenar los identificadores de objeto para la operación masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="c788e-120">La función ReadContentPropertiesBulk del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de recuperación masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="c788e-121">La primera tarea que se lleva a cabo en este ejemplo es determinar si el controlador especificado admite operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="c788e-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="c788e-122">Esto se logra llamando a QueryInterface en la interfaz IPortableDeviceProperties y comprobando la existencia de IPortableDevicePropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="c788e-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


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



<span data-ttu-id="c788e-123">Si el controlador admite operaciones masivas, el paso siguiente consiste en crear una instancia de la [**interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) y especificar las claves correspondientes a las propiedades que recuperará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c788e-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="c788e-124">Para obtener una descripción de este proceso, vea el tema [recuperar propiedades de un solo objeto](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c788e-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="c788e-125">Una vez especificadas las claves apropiadas, la aplicación de ejemplo crea una instancia de la [**interfaz IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="c788e-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="c788e-126">La aplicación usará los métodos de esta interfaz para realizar el seguimiento del progreso de la operación asincrónica de recuperación masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="c788e-127">La siguiente función a la que llama la aplicación de ejemplo es la función auxiliar CreateIPortableDevicePropVariantCollectionWithAllObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="c788e-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="c788e-128">Esta función crea una lista de todos los identificadores de objetos disponibles para fines de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c788e-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="c788e-129">(Una aplicación real limitaría la lista de identificadores a un conjunto determinado de objetos.</span><span class="sxs-lookup"><span data-stu-id="c788e-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="c788e-130">Por ejemplo, una aplicación puede crear una lista de identificadores para todos los objetos que se encuentran actualmente en una vista de carpeta determinada).</span><span class="sxs-lookup"><span data-stu-id="c788e-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="c788e-131">Como se indicó anteriormente, la función auxiliar enumera de forma recursiva todos los objetos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="c788e-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="c788e-132">Devuelve esta lista en una [**interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene un identificador para cada objeto encontrado.</span><span class="sxs-lookup"><span data-stu-id="c788e-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="c788e-133">La función auxiliar se define en el módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="c788e-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="c788e-134">Una vez que se hayan realizado los pasos anteriores, la aplicación de ejemplo inicia la recuperación de la propiedad asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c788e-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="c788e-135">Para ello, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c788e-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="c788e-136">Llamando a IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, que pone en cola una solicitud para la recuperación de la propiedad masiva.</span><span class="sxs-lookup"><span data-stu-id="c788e-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="c788e-137">(Tenga en cuenta que aunque la solicitud se pone en cola, no se inicia).</span><span class="sxs-lookup"><span data-stu-id="c788e-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="c788e-138">Llamando a IPortableDevicePropertiesBulk:: Start para iniciar la solicitud en cola.</span><span class="sxs-lookup"><span data-stu-id="c788e-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="c788e-139">Estos pasos se muestran en el siguiente fragmento de código de la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c788e-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
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
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a><span data-ttu-id="c788e-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c788e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c788e-141">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="c788e-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="c788e-142">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="c788e-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="c788e-143">**Interfaz IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="c788e-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="c788e-144">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="c788e-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="c788e-145">**Interfaz IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="c788e-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="c788e-146">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c788e-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="c788e-147">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="c788e-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



