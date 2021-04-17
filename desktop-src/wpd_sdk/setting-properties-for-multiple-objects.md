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
# <a name="setting-properties-for-multiple-objects"></a>Establecer las propiedades de varios objetos

Algunos controladores de dispositivos admiten la configuración de propiedades de varios objetos en una única llamada de función, lo que se conoce como una escritura masiva. La aplicación puede realizar una escritura masiva con las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso a los métodos específicos del contenido.             |
| [**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Proporciona acceso a los métodos específicos de la propiedad.            |
| [**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Admite la operación de escritura masiva.                           |
| [**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Se utiliza para almacenar los identificadores de objeto para la operación masiva. |
| [**Interfaz IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)           | Se utiliza para identificar las propiedades que se van a escribir.               |



 

La `WriteContentPropertiesBulk` función del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de escritura masiva.

La primera tarea que se lleva a cabo en este ejemplo es determinar si el controlador especificado admite operaciones masivas. Esto se logra llamando a QueryInterface en un objeto **IPortableDeviceProperties** y comprobando la existencia de **IPortableDevicePropertiesBulk**.


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



La siguiente tarea implica la creación de un objeto **IPortableDeviceValuesCollection** . Este es el objeto que contiene los valores de propiedad que escribirá el ejemplo.


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



Después de esto, el ejemplo crea una instancia de la [**interfaz IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). La aplicación usará los métodos de esta interfaz para realizar el seguimiento del progreso de la operación de escritura masiva asincrónica.


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



La siguiente función a la que llama la aplicación de ejemplo es la `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` función auxiliar. Esta función enumera de forma recursiva todos los objetos en un dispositivo determinado y devuelve una [**interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene un identificador para cada objeto encontrado. Esta función se define en el módulo ContentEnumeration. cpp.


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



El objeto **IPortableDevicePropVariantCollection** contiene una colección de valores **PROPVARIANT** indizados del mismo VARTYPE. En este caso, estos valores contienen un identificador de objeto determinado para cada objeto que se encuentra en el dispositivo.

Los identificadores de objeto y sus propiedades de nombre respectivas se almacenan en un objeto [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) . Las propiedades de nombre están organizadas de modo que al primer objeto se le asigna una propiedad de nombre de "NewName0", al segundo objeto se le asigna una propiedad de nombre de "NewName1", y así sucesivamente.

En el siguiente fragmento del ejemplo se muestra cómo se inicializó el objeto **IPortableDeviceValuesCollection** con identificadores de objeto y nuevas cadenas de nombre.


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



Una vez que el ejemplo crea el objeto **IPortableDeviceValuesCollection** que contiene los pares de nombre y identificador de objeto, puede comenzar la operación asincrónica.

La operación de escritura asincrónica comienza cuando el ejemplo llama al método [**IPortableDevicePropertiesBulk:: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) . Este método notifica al controlador que una operación masiva está a punto de comenzar. Después de esto, el ejemplo llama al método [**IPortableDeviceBulk:: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) para empezar a escribir realmente los nuevos valores de nombre.


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



Tenga en cuenta que el ejemplo espera un período de tiempo infinitamente largo para que se complete la operación. Si se trata de una aplicación de producción, es necesario modificar el código.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



