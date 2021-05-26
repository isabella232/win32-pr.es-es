---
description: Escribir propiedades de objeto
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Escribir propiedades de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726501c986e73033437de3bee0c11b3beb66150d
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423935"
---
# <a name="writing-object-properties"></a><span data-ttu-id="fc969-103">Escribir propiedades de objeto</span><span class="sxs-lookup"><span data-stu-id="fc969-103">Writing Object Properties</span></span>

<span data-ttu-id="fc969-104">Los servicios suelen contener objetos secundarios que pertenecen a uno de los formatos que admite cada servicio.</span><span class="sxs-lookup"><span data-stu-id="fc969-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="fc969-105">Por ejemplo, un servicio Contactos puede admitir varios objetos de contacto con el formato de contacto abstracto.</span><span class="sxs-lookup"><span data-stu-id="fc969-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="fc969-106">Cada objeto de contacto se describe mediante propiedades relacionadas (nombre de contacto, número de teléfono, dirección de correo electrónico, y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="fc969-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="fc969-107">La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede actualizar la propiedad name de un objeto secundario del servicio Contacts determinado.</span><span class="sxs-lookup"><span data-stu-id="fc969-107">The WpdServicesApiSample application includes code that demonstrates how an application can update the name property for a child object of the given Contacts service.</span></span> <span data-ttu-id="fc969-108">En este ejemplo se usan las siguientes interfaces WPD.</span><span class="sxs-lookup"><span data-stu-id="fc969-108">This sample uses the following WPD interfaces.</span></span>



| <span data-ttu-id="fc969-109">Interfaz</span><span class="sxs-lookup"><span data-stu-id="fc969-109">Interface</span></span>                                                      | <span data-ttu-id="fc969-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc969-110">Description</span></span>                                                                                                                                                          |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc969-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="fc969-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | <span data-ttu-id="fc969-112">Se usa para recuperar la **interfaz IPortableDeviceContent2** para acceder a los métodos de servicio admitidos.</span><span class="sxs-lookup"><span data-stu-id="fc969-112">Used to retrieve the **IPortableDeviceContent2** interface to access the supported service methods.</span></span>                                                                  |
| [<span data-ttu-id="fc969-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="fc969-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | <span data-ttu-id="fc969-114">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="fc969-114">Provides access to the content-specific methods.</span></span>                                                                                                                     |
| [<span data-ttu-id="fc969-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="fc969-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="fc969-116">Se usa para escribir los valores de propiedad del objeto y para determinar si se puede escribir una propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="fc969-116">Used to write the object property values and to determine whether a given property can be written</span></span>                                                                    |
| [<span data-ttu-id="fc969-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="fc969-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="fc969-118">Se usa para contener los valores de propiedad que se escribirán, determinar los resultados de la operación de escritura y recuperar atributos de propiedades (al determinar la funcionalidad de escritura).</span><span class="sxs-lookup"><span data-stu-id="fc969-118">Used to hold the property values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="fc969-119">Cuando el usuario elige la opción "8" en la línea de comandos, la aplicación invoca el método **WriteContentProperties** que se encuentra en el módulo ContentProperties.cpp.</span><span class="sxs-lookup"><span data-stu-id="fc969-119">When the user chooses option "8" at the command line, the application invokes the **WriteContentProperties** method that is found in the ContentProperties.cpp module.</span></span> <span data-ttu-id="fc969-120">Este método solicita al usuario que escriba un identificador de objeto para la propiedad que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="fc969-120">This method prompts the user to enter an object identifier for the property to be updated.</span></span> <span data-ttu-id="fc969-121">El usuario identifica el objeto y el método solicita al usuario que especifique un nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="fc969-121">The user identifies the object, and the method prompts the user to specify a new name.</span></span> <span data-ttu-id="fc969-122">Una vez especificado este nombre, el método actualiza la propiedad Name para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="fc969-122">After this name is specified, the method updates the Name property for the given object.</span></span>

<span data-ttu-id="fc969-123">Tenga en cuenta que antes de escribir las propiedades del objeto, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="fc969-123">Note that prior to writing the object properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="fc969-124">El código siguiente para el **método WriteContentProperties** muestra cómo la aplicación usa la interfaz [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar una [**interfaz IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)</span><span class="sxs-lookup"><span data-stu-id="fc969-124">The following code for the **WriteContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="fc969-125">Al pasar propertykeys de las propiedades solicitadas al método [**IPortableDeviceProperties::SetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **WriteContentProperties** actualiza la propiedad name.</span><span class="sxs-lookup"><span data-stu-id="fc969-125">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **WriteContentProperties** updates the name property.</span></span>


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
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

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
 }
}
```



## <a name="related-topics"></a><span data-ttu-id="fc969-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc969-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc969-127">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="fc969-127">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="fc969-128">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="fc969-128">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="fc969-129">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="fc969-129">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



