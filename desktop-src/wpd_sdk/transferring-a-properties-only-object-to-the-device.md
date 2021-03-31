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
# <a name="transferring-a-properties-only-object-to-the-device"></a>Transferir un objeto Properties-Only al dispositivo

Aunque en el ejemplo del tema anterior se mostró la creación de contenido en un dispositivo que consta de propiedades y datos, este tema se centra en la creación de un objeto de solo propiedades.

Las transferencias de solo propiedades se realizan mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                          | Descripción                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Proporciona acceso a los métodos específicos del contenido.       |
| [**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)   | Se utiliza para recuperar las propiedades que describen el contenido. |



 

La `TransferContactToDevice` función del módulo ContentTransfer. cpp de la aplicación de ejemplo muestra cómo una aplicación podría transferir información de contacto de un equipo a un dispositivo conectado. En este ejemplo concreto, el nombre de contacto transferido es una "John Kane" codificada de forma rígida y el número de teléfono del contacto transferido siempre es "425-555-0123".

La primera tarea que se realiza mediante la `TransferContactToDevice` función es solicitar al usuario que escriba un identificador de objeto para el objeto primario en el dispositivo (con el que se transferirá el contenido).


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



El siguiente paso es la recuperación de las propiedades de contacto, que se usarán cuando el ejemplo escriba el nuevo contacto en el dispositivo. La función auxiliar realiza la recuperación de propiedades de contacto `GetRequiredPropertiesForPropertiesOnlyContact` .


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



Esta función escribe los datos siguientes en un objeto **IPortableDeviceValues** .

-   Identificador de objeto del elemento primario del contacto en el dispositivo. (Este es el destino en el que el dispositivo almacenará el objeto).
-   El tipo de objeto (un contacto).
-   El nombre de contacto (una cadena codificada de "John Kane").
-   El número de teléfono de contacto (una cadena codificada de forma rígida de "425-555-0123").

En el último paso se crea el objeto de solo propiedades en el dispositivo (con las propiedades establecidas por la `GetRequiredPropertiesForPropertiesOnlyContact` función auxiliar). Esto se logra mediante una llamada al método **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .


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

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



