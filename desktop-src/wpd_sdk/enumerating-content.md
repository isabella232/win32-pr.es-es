---
description: Enumerar contenido
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerar contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666479"
---
# <a name="enumerating-content"></a>Enumerar contenido

El contenido de un dispositivo (ya sea una carpeta, una libreta de teléfonos, un vídeo o una imagen fija) se denomina objeto en la API de WPD. Los identificadores de objeto hacen referencia a estos objetos y se describen mediante propiedades. Puede enumerar los objetos en un dispositivo mediante la llamada a métodos en la [**interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), la [**interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)y la [**interfaz IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).

En la aplicación de ejemplo se muestra la enumeración de contenido en la función EnumerateAllContent que se encuentra en el módulo ContentEnumeration. cpp. Esta función, a su vez, llama a una función RecursiveEnumerate que recorre la jerarquía de objetos encontrados en el dispositivo seleccionado y devuelve un identificador de objeto para cada objeto.

Como se indicó, la función RecursiveEnumerate recupera un identificador de objeto para cada objeto encontrado en el dispositivo. El identificador de objeto es un valor de cadena. Una vez que la aplicación recupera este identificador, puede obtener información más descriptiva del objeto (por ejemplo, el nombre del objeto, el identificador del elemento primario del objeto, etc.). Esta información descriptiva se conoce como propiedades del objeto (o metadatos). La aplicación puede recuperar estas propiedades llamando a los miembros de la [**interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).

La función EnumerateAllContent comienza mediante la recuperación de un puntero a una [**interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Recupera este puntero llamando al método [**IPortableDevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Una vez que recupera el puntero a la interfaz IPortableDeviceContent, la función EnumerateAllContent llama a la función RecursiveEnumerate, que recorre la jerarquía de objetos encontrados en el dispositivo dado y devuelve un identificador de objeto para cada uno.

La función RecursiveEnumerate comienza mediante la recuperación de un puntero a una [**interfaz IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Esta interfaz expone los métodos que utiliza una aplicación para navegar por la lista de objetos encontrados en un dispositivo determinado.

En este ejemplo, la función RecursiveEnumerate llama al método [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) para atravesar la lista de objetos.

Cada llamada al método [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) solicita un lote de 10 identificadores. (El valor se especifica mediante el parámetro NUM \_ OBJETOS \_ para \_ solicitar una constante que se proporciona como primer argumento).


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



