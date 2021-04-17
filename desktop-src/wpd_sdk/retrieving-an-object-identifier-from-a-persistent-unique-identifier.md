---
description: Recuperar un identificador de objeto de un identificador único persistente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recuperar un identificador de objeto de un identificador único persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716576"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Recuperar un identificador de objeto de un identificador único persistente

Solo se garantiza que los identificadores de objeto son únicos para una sesión de dispositivo determinada; Si el usuario establece una nueva conexión, es posible que los identificadores de una sesión anterior no coincidan con los identificadores de la sesión actual. Para resolver este problema, la API de WPD admite identificadores únicos persistentes (PUID), que se conservan en las sesiones de dispositivo.

Algunos dispositivos almacenan sus PUID de forma nativa con un objeto determinado. Otros pueden generar el PUID basándose en un hash de los datos del objeto seleccionado. Otros pueden tratar identificadores de objeto como PUID (porque pueden garantizar que estos identificadores nunca cambian).

La función GetObjectIdentifierFromPersistentUniqueIdentifier del módulo ContentProperties. cpp muestra la recuperación de un identificador de objeto para un PUID determinado.

La aplicación puede recuperar un identificador de objeto para un PUID correspondiente mediante las interfaces descritas en la tabla siguiente.



| Interfaz                                                                                      | Descripción                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Proporciona acceso al método de recuperación.                                                            |
| [**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Se utiliza para almacenar el identificador de objeto y el identificador único persistente (PUID) correspondiente. |



 

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



Después, la aplicación de ejemplo recupera un objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que se usará para invocar el método [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .


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



A continuación, crea un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contendrá el PUID proporcionado por el usuario.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Una vez realizados los tres pasos anteriores, el ejemplo está listo para recuperar el identificador de objeto que coincide con el PUID proporcionado por el usuario. Esto se logra mediante una llamada al método [**IPortableDeviceContent:: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) . Antes de llamar a este método, el ejemplo Inicializa una estructura PROPVARIANT, escribe el PUID proporcionado por el usuario en esta estructura y lo agrega al objeto IPortableDevicePropVariantCollection en el que pPersistentUniqueIDs apunta. Este puntero se pasa como primer argumento al método GetObjectIDsFromPersistentUniqueIDs. El segundo argumento de GetObjectIDsFromPersistentUniqueIDs es un objeto IPortableDevicePropVariantCollection que recibe el identificador de objeto coincidente.


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

[**Interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaz IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 



