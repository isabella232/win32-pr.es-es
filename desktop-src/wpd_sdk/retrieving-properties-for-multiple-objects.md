---
description: Recuperar propiedades para varios objetos
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recuperar propiedades para varios objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1ad9ec397daa90c149fe950c1fc4777c407e3f5f3a359f46cf8bef56e18b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083519"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Recuperar propiedades para varios objetos

Algunos controladores de dispositivos admiten la recuperación de propiedades para varios objetos en una sola llamada de función. esto se conoce como recuperación masiva. Hay dos tipos de operaciones de recuperación masiva: el primer tipo recupera las propiedades de una lista de objetos y el segundo tipo recupera las propiedades de todos los objetos de un formato determinado. En el ejemplo descrito en esta sección se muestra lo primero.

La aplicación puede realizar una recuperación masiva mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso a los métodos específicos del contenido.                   |
| [**IPortableDeviceKeyCollection (Interfaz)**](iportabledevicekeycollection.md)                 | Se usa para identificar las propiedades que se recuperarán.                   |
| [**IPortableDeviceProperties (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Se usa para determinar si un controlador determinado admite operaciones masivas. |
| [**IPortableDevicePropertiesBulk (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Admite la operación de recuperación masiva.                             |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para almacenar los identificadores de objeto para la operación masiva.       |



 

La función ReadContentPropertiesBulk del módulo ContentProperties.cpp de la aplicación de ejemplo muestra una operación de recuperación masiva.

La primera tarea que se realiza en este ejemplo es determinar si el controlador determinado admite o no operaciones masivas. Esto se logra llamando a QueryInterface en la interfaz IPortableDeviceProperties y comprobando la existencia de IPortableDevicePropertiesBulk.


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



Si el controlador admite operaciones masivas, el siguiente paso es crear una instancia de la interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) y especificar las claves que corresponden a las propiedades que recuperará la aplicación. Para obtener una descripción de este proceso, vea el [tema Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) .

Una vez especificadas las claves adecuadas, la aplicación de ejemplo crea una instancia de la [**interfaz IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). La aplicación usará los métodos de esta interfaz para realizar un seguimiento del progreso de la operación asincrónica de recuperación masiva.


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



La siguiente función a la que llama la aplicación de ejemplo es la función auxiliar CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Esta función crea una lista de todos los identificadores de objeto disponibles para fines de ejemplo. (Una aplicación real limitaría la lista de identificadores a un conjunto determinado de objetos. Por ejemplo, una aplicación puede crear una lista de identificadores para todos los objetos que se encuentran actualmente en una vista de carpeta determinada).

Como se indicó anteriormente, la función auxiliar enumera de forma recursiva todos los objetos de un dispositivo determinado. Devuelve esta lista en una [**interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene un identificador para cada objeto que encontró. La función auxiliar se define en el módulo ContentEnumeration.cpp.


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



Una vez que se han realizado los pasos anteriores, la aplicación de ejemplo inicia la recuperación de la propiedad asincrónica. Para ello, haga lo siguiente:

1.  Llamar a IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, que pone en cola una solicitud para la recuperación masiva de propiedades. (Tenga en cuenta que, aunque la solicitud está en cola, no se inicia).
2.  Llamar a IPortableDevicePropertiesBulk::Start para iniciar la solicitud en cola.

Estos pasos se muestran en el siguiente extracto de código de la aplicación de ejemplo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDevice (Interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection (Interfaz)**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties (Interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



