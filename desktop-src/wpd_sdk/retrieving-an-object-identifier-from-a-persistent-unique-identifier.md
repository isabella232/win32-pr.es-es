---
description: Recuperar un identificador de objeto a partir de un identificador único persistente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recuperar un identificador de objeto a partir de un identificador único persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054775"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Recuperar un identificador de objeto a partir de un identificador único persistente

Solo se garantiza que los identificadores de objeto sean únicos para una sesión de dispositivo determinada. Si el usuario establece una nueva conexión, es posible que los identificadores de una sesión anterior no coincidan con los identificadores de la sesión actual. Para resolver este problema, la API de WPD admite identificadores únicos persistentes (PUID), que se conservan entre sesiones de dispositivo.

Algunos dispositivos almacenan sus PUID de forma nativa con un objeto determinado. Otros pueden generar el PUID basándose en un hash de los datos de objeto seleccionados. Otros pueden tratar los identificadores de objeto como PUID (porque pueden garantizar que estos identificadores nunca cambien).

La función GetObjectIdentifierFromPersistentUniqueIdentifier del módulo ContentProperties.cpp muestra la recuperación de un identificador de objeto para un PUID determinado.

La aplicación puede recuperar un identificador de objeto para un PUID correspondiente mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso al método de recuperación.                                                            |
| [**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md) | Se usa para almacenar el identificador de objeto y el identificador único persistente (PUID) correspondiente. |



 

La primera tarea que realiza la aplicación de ejemplo es obtener un PUID del usuario.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Después de esto, la aplicación de ejemplo recupera un objeto [**IPortableDeviceContent,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) que usará para invocar el [**método GetObjectIDsFromPersistentUniqueIDs.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids)


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



A continuación, crea [**un objeto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contendrán el PUID proporcionado por el usuario.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Una vez que se han realizado los tres pasos anteriores, el ejemplo está listo para recuperar el identificador de objeto que coincide con el PUID proporcionado por el usuario. Esto se logra llamando al método [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) Antes de llamar a este método, el ejemplo inicializa una estructura PROPVARIANT, escribe el PUID proporcionado por el usuario en esta estructura y lo agrega al objeto IPortableDevicePropVariantCollection en el que apunta pPersistentUniqueIDs. Este puntero se pasa como primer argumento al método GetObjectIDsFromPersistentUniqueIDs. El segundo argumento de GetObjectIDsFromPersistentUniqueIDs es un objeto IPortableDevicePropVariantCollection que recibe el identificador de objeto correspondiente.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDevice (Interfaz)**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent (interfaz)**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDevicePropVariantCollection (Interfaz)**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



