---
description: Recuperar propiedades para un solo objeto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recuperar propiedades para un solo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0806de3da9cd3f0674057d413a071996f86f5d74a364c0f5db707965fc2220
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054725"
---
# <a name="retrieving-properties-for-a-single-object"></a>Recuperar propiedades para un solo objeto

Una vez que la aplicación recupera un identificador de objeto (vea el tema [Enumeración](enumerating-content.md) de contenido) para un objeto determinado, puede recuperar información descriptiva sobre ese objeto llamando a métodos en la interfaz [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) y la interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).

El [**método IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera una lista de propiedades especificadas para un objeto determinado. (La aplicación también podría llamar al método GetValues y especificar un valor **NULL** para el parámetro pKeys para recuperar todas las propiedades de un objeto determinado; sin embargo, el rendimiento de este método puede ser significativamente más lento al recuperar todas las propiedades).

Sin embargo, antes de que la aplicación llame a GetValues, debe identificar las propiedades que se deben recuperar estableciendo las claves correspondientes en un [**objeto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md). La aplicación identificará las propiedades de interés llamando al método [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) y suministrando un valor PROPERTYKEY que identifica cada propiedad que recuperará.

La función ReadContentProperties del módulo ContentProperties.cpp de la aplicación de ejemplo muestra cómo se recuperaron las cinco propiedades de un objeto seleccionado. En la tabla siguiente se describe cada una de estas propiedades y su valor REFPROPERTYKEY correspondiente.



| Propiedad                     | Descripción                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Identificador de objeto primario     | Cadena que especifica el identificador del elemento primario del objeto especificado.                                                                            | IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD             |
| Nombre del objeto                  | Cadena que especifica el nombre del objeto especificado.                                                                                            | NOMBRE DE OBJETO \_ \_ WPD                   |
| Identificador único persistente | Cadena que especifica un identificador único para el objeto especificado. (Este identificador es persistente entre sesiones, a diferencia del identificador de objeto). | IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD |
| Formato de objeto                | Identificador único global (GUID) que especifica el formato del archivo correspondiente a un objeto determinado.                                       | FORMATO DE OBJETO \_ \_ WPD                 |
| Tipo de contenido de objeto          | GUID que especifica el tipo de contenido asociado a un objeto determinado.                                                                        | TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD          |



 

El siguiente extracto de la función ReadContentProperties muestra cómo la aplicación de ejemplo usó la interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) y el método [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) para identificar las propiedades que recuperaría.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Una vez que la aplicación de ejemplo estableció las claves adecuadas, llamó al método [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) para recuperar los valores especificados para el objeto especificado.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDevice (interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceKeyCollection (interfaz)**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



