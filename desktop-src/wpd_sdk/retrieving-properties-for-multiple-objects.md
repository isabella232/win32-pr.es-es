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
# <a name="retrieving-properties-for-multiple-objects"></a>Recuperar propiedades de varios objetos

Algunos controladores de dispositivos admiten la recuperación de propiedades de varios objetos en una única llamada de función; Esto se conoce como recuperación masiva. Hay dos tipos de operaciones de recuperación masiva: el primer tipo recupera las propiedades de una lista de objetos y el segundo tipo recupera las propiedades de todos los objetos de un formato determinado. En el ejemplo descrito en esta sección se muestra el anterior.

La aplicación puede realizar una recuperación masiva con las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso a los métodos específicos del contenido.                   |
| [**Interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Se utiliza para identificar las propiedades que se van a recuperar.                   |
| [**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Se utiliza para determinar si un controlador determinado admite operaciones masivas. |
| [**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Admite la operación de recuperación masiva.                             |
| [**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Se utiliza para almacenar los identificadores de objeto para la operación masiva.       |



 

La función ReadContentPropertiesBulk del módulo ContentProperties. cpp de la aplicación de ejemplo muestra una operación de recuperación masiva.

La primera tarea que se lleva a cabo en este ejemplo es determinar si el controlador especificado admite operaciones masivas. Esto se logra llamando a QueryInterface en la interfaz IPortableDeviceProperties y comprobando la existencia de IPortableDevicePropertiesBulk.


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



Si el controlador admite operaciones masivas, el paso siguiente consiste en crear una instancia de la [**interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) y especificar las claves correspondientes a las propiedades que recuperará la aplicación. Para obtener una descripción de este proceso, vea el tema [recuperar propiedades de un solo objeto](retrieving-properties-for-a-single-object.md) .

Una vez especificadas las claves apropiadas, la aplicación de ejemplo crea una instancia de la [**interfaz IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). La aplicación usará los métodos de esta interfaz para realizar el seguimiento del progreso de la operación asincrónica de recuperación masiva.


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



La siguiente función a la que llama la aplicación de ejemplo es la función auxiliar CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Esta función crea una lista de todos los identificadores de objetos disponibles para fines de ejemplo. (Una aplicación real limitaría la lista de identificadores a un conjunto determinado de objetos. Por ejemplo, una aplicación puede crear una lista de identificadores para todos los objetos que se encuentran actualmente en una vista de carpeta determinada).

Como se indicó anteriormente, la función auxiliar enumera de forma recursiva todos los objetos de un dispositivo determinado. Devuelve esta lista en una [**interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene un identificador para cada objeto encontrado. La función auxiliar se define en el módulo ContentEnumeration. cpp.


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



Una vez que se hayan realizado los pasos anteriores, la aplicación de ejemplo inicia la recuperación de la propiedad asincrónica. Para ello, haga lo siguiente:

1.  Llamando a IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, que pone en cola una solicitud para la recuperación de la propiedad masiva. (Tenga en cuenta que aunque la solicitud se pone en cola, no se inicia).
2.  Llamando a IPortableDevicePropertiesBulk:: Start para iniciar la solicitud en cola.

Estos pasos se muestran en el siguiente fragmento de código de la aplicación de ejemplo.


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

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interfaz IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



