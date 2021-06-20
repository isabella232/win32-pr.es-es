---
title: Recuperación de propiedades de objetos WPD
description: La aplicación WpdServiceApiSample muestra cómo una aplicación puede recuperar las propiedades de objeto de contenido compatibles con un servicio Contacts determinado.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404318"
---
# <a name="retrieving-wpd-object-properties"></a>Recuperación de propiedades de objetos WPD

Los servicios suelen contener objetos secundarios que pertenecen a uno de los formatos que admite cada servicio. Por ejemplo, un servicio Contactos puede admitir varios objetos de contacto con el formato abstracto Contacto. Cada objeto de contacto se describe mediante propiedades relacionadas (nombre de contacto, número de teléfono, dirección de correo electrónico, entre otras).

La aplicación WpdServiceApiSample incluye código que muestra cómo una aplicación puede recuperar las propiedades content-object admitidas por un servicio Contacts determinado. En este ejemplo se usan las interfaces siguientes.



| Interfaz | Descripción    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Recupera la interfaz **IPortableDeviceContent2** para acceder a los métodos de servicio admitidos. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Proporciona acceso a los métodos específicos del contenido.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Recupera los valores de propiedad del objeto.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Contiene los valores de propiedad que se leyeron para ese objeto.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Contiene los parámetros de un método determinado.                                                  |



 

Cuando el usuario elige la opción "7" en la línea de comandos, la aplicación invoca el método **ReadContentProperties** que se encuentra en el módulo ContentProperties.cpp.

Este método recupera las cuatro propiedades siguientes para el objeto de contacto especificado.



| Propiedad                     | Descripción                                                                                                                                                                                                      | Device Services PROPERTYKEY     | PROPERTYKEY de WPD \_ equivalente         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Identificador de objeto primario     | Cadena que especifica el identificador del elemento primario del objeto especificado.                                                                                                                                            | PKEY \_ GenericObj \_ ParentID      | IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD             |
| Nombre del objeto                  | Cadena que especifica el nombre del objeto especificado                                                                                                                                                             | PKEY \_ GenericObj \_ Name          | NOMBRE DE OBJETO \_ \_ WPD                   |
| Identificador único persistente | Cadena que especifica un identificador único para el objeto especificado. Este identificador es persistente entre sesiones, a diferencia del identificador de objeto. Para los servicios, debe ser una representación de cadena de un GUID. | PKEY \_ GenericObj \_ PersistentUID | WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID |
| Formato de objeto                | Identificador único global (GUID) que especifica el formato del archivo correspondiente a un objeto determinado.                                                                                                        | PKEY \_ GenericObj \_ ObjectFormat  | FORMATO DE OBJETO \_ \_ WPD                 |



 

-   Id. primario
-   Nombre
-   PersistentUID
-   Formato

Tenga en cuenta que antes de recuperar las propiedades de contenido, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.

El código siguiente para el **método ReadContentProperties** muestra cómo la aplicación usa la interfaz [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) para recuperar una [**interfaz IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) Al pasar propertykeys de las propiedades solicitadas al método [**IPortableDeviceProperties::GetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **ReadContentProperties** recupera los valores solicitados y, a continuación, los muestra en la ventana de la consola.


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
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

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



