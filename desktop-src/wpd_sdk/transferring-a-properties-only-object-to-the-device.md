---
description: Transferir un Properties-Only al dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Transferir un Properties-Only al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466651"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a>Transferir un Properties-Only al dispositivo

Aunque en el ejemplo del tema anterior se mostró la creación de contenido en un dispositivo que consta de propiedades y datos, este tema se centra en la creación de un objeto de solo propiedades.

Las transferencias de solo propiedad se logran mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                          | Descripción                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Proporciona acceso a los métodos específicos del contenido.       |
| [**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)   | Se usa para recuperar las propiedades que describen el contenido. |



 

La `TransferContactToDevice` función del módulo ContentTransfer.cpp de la aplicación de ejemplo muestra cómo una aplicación podría transferir información de contacto desde un equipo a un dispositivo conectado. En este ejemplo en particular, el nombre de contacto transferido es un "John Transfer" codificado de forma fuerte y el número de teléfono de contacto transferido siempre es "425-555-0123".

La primera tarea que realiza la función es pedir al usuario que escriba un identificador de objeto para el objeto primario en el dispositivo (bajo el que se transferirá `TransferContactToDevice` el contenido).


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



El siguiente paso es la recuperación de las propiedades de contacto, que se usarán cuando el ejemplo escriba el nuevo contacto en el dispositivo. La función auxiliar realiza la recuperación de las propiedades `GetRequiredPropertiesForPropertiesOnlyContact` de contacto.


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



Esta función escribe los datos siguientes en un **objeto IPortableDeviceValues.**

-   Identificador de objeto del elemento primario del contacto en el dispositivo. (Este es el destino donde el dispositivo almacenará el objeto).
-   Tipo de objeto (un contacto).
-   El nombre del contacto (una cadena codificada de forma codificada de forma codificada como "John John")
-   El número de teléfono de contacto (una cadena codificada de forma hard de "425-555-0123").

El paso final crea el objeto de solo propiedades en el dispositivo (mediante las propiedades establecidas por la `GetRequiredPropertiesForPropertiesOnlyContact` función auxiliar). Para ello, se llama al **método IPortableDeviceContent::CreateObjectWithPropertiesOnly.**


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDevice (Interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceValues (Interfaz)**](iportabledevicevalues.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



