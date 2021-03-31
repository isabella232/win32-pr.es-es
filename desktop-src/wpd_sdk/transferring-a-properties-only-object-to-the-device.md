---
description: Transferir un objeto Properties-Only al dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Transferir un objeto Properties-Only al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816291"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="47e14-103">Transferir un objeto Properties-Only al dispositivo</span><span class="sxs-lookup"><span data-stu-id="47e14-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="47e14-104">Aunque en el ejemplo del tema anterior se mostró la creación de contenido en un dispositivo que consta de propiedades y datos, este tema se centra en la creación de un objeto de solo propiedades.</span><span class="sxs-lookup"><span data-stu-id="47e14-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="47e14-105">Las transferencias de solo propiedades se realizan mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="47e14-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="47e14-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="47e14-106">Interface</span></span>                                                          | <span data-ttu-id="47e14-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="47e14-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="47e14-108">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="47e14-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="47e14-109">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="47e14-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="47e14-110">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="47e14-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="47e14-111">Se utiliza para recuperar las propiedades que describen el contenido.</span><span class="sxs-lookup"><span data-stu-id="47e14-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="47e14-112">La `TransferContactToDevice` función del módulo ContentTransfer. cpp de la aplicación de ejemplo muestra cómo una aplicación podría transferir información de contacto de un equipo a un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="47e14-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="47e14-113">En este ejemplo concreto, el nombre de contacto transferido es una "John Kane" codificada de forma rígida y el número de teléfono del contacto transferido siempre es "425-555-0123".</span><span class="sxs-lookup"><span data-stu-id="47e14-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="47e14-114">La primera tarea que se realiza mediante la `TransferContactToDevice` función es solicitar al usuario que escriba un identificador de objeto para el objeto primario en el dispositivo (con el que se transferirá el contenido).</span><span class="sxs-lookup"><span data-stu-id="47e14-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="47e14-115">El siguiente paso es la recuperación de las propiedades de contacto, que se usarán cuando el ejemplo escriba el nuevo contacto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e14-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="47e14-116">La función auxiliar realiza la recuperación de propiedades de contacto `GetRequiredPropertiesForPropertiesOnlyContact` .</span><span class="sxs-lookup"><span data-stu-id="47e14-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="47e14-117">Esta función escribe los datos siguientes en un objeto **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="47e14-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="47e14-118">Identificador de objeto del elemento primario del contacto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e14-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="47e14-119">(Este es el destino en el que el dispositivo almacenará el objeto).</span><span class="sxs-lookup"><span data-stu-id="47e14-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="47e14-120">El tipo de objeto (un contacto).</span><span class="sxs-lookup"><span data-stu-id="47e14-120">The object type (a contact).</span></span>
-   <span data-ttu-id="47e14-121">El nombre de contacto (una cadena codificada de "John Kane").</span><span class="sxs-lookup"><span data-stu-id="47e14-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="47e14-122">El número de teléfono de contacto (una cadena codificada de forma rígida de "425-555-0123").</span><span class="sxs-lookup"><span data-stu-id="47e14-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="47e14-123">En el último paso se crea el objeto de solo propiedades en el dispositivo (con las propiedades establecidas por la `GetRequiredPropertiesForPropertiesOnlyContact` función auxiliar).</span><span class="sxs-lookup"><span data-stu-id="47e14-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="47e14-124">Esto se logra mediante una llamada al método **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .</span><span class="sxs-lookup"><span data-stu-id="47e14-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="47e14-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47e14-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e14-126">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="47e14-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="47e14-127">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="47e14-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="47e14-128">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="47e14-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="47e14-129">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="47e14-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



