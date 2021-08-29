---
title: Exploración de un dispositivo
description: Exploración de un dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Administrador de dispositivos, exploración de dispositivos
- Administrador de dispositivos, explorar dispositivos
- guía de programación, exploración de dispositivos
- aplicaciones de escritorio, exploración de dispositivos
- crear Windows aplicaciones de Administrador de dispositivos multimedia, explorar dispositivos
- exploración de dispositivos
- Almacenajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfdefbf5d71563cae2bb5b78383cfe0582e0af04e447e78166d0e80fda536d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957585"
---
# <a name="exploring-a-device"></a>Exploración de un dispositivo

Explorar un dispositivo es similar a explorar una unidad de disco. Todos los objetos de un dispositivo se *denominan almacenamientos.* Un almacenamiento puede ser un archivo, una carpeta u un objeto abstracto (por ejemplo, una lista de reproducción) en el dispositivo. Debe examinar los atributos y metadatos de un almacenamiento (si se admite) para comprender qué tipo de almacenamiento es. Los almacenamientos se organizan jerárquicamente en el dispositivo; cada almacenamiento tiene exactamente un elemento primario y, en última instancia, todos los almacenamientos descienden de un único almacenamiento de dispositivo raíz, normalmente denominado \\ "".

En los pasos siguientes se describe cómo explorar un dispositivo:

1.  Obtenga la [**interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) de un dispositivo como se describe en [Enumeración de dispositivos.](enumerating-devices.md)
2.  Llame [**a IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) para recuperar una [**interfaz IWMDMEnumStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) Esta interfaz se usa para obtener todos los objetos secundarios del almacenamiento que devuelve esta interfaz. Al obtener esta interfaz del dispositivo, como estamos aquí, solo contendrán un almacenamiento: el almacenamiento raíz del dispositivo.
3.  Llame a [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) con un recuento de 1 para recuperar la interfaz [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) para el almacenamiento del dispositivo raíz. (No se puede solicitar más de un elemento secundario desde el dispositivo).
4.  Examine todos los almacenamientos del dispositivo mediante una llamada recursiva a [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) y, a continuación, **IWMDMEnumStorage::Next** para obtener los secundarios de un almacenamiento. Para ver si un almacenamiento tiene secundarios para evitar las llamadas a **EnumStorage** y **Next**, puede llamar a [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para buscar las marcas WMDM STORAGE ATTR HAS FILES o \_ \_ \_ \_ WMDM \_ STORAGE \_ ATTR HAS \_ \_ FOLDERS. Para obtener más información sobre cómo obtener [](getting-and-setting-metadata-and-attributes.md) las propiedades de un almacenamiento, vea Obtener y establecer metadatos y atributos y Obtener y establecer metadatos y [atributos en la aplicación](getting-and-setting-metadata-and-attributes-in-the-application.md).

Windows El Administrador de dispositivos no expone un conjunto estándar de carpetas para contener medios de un tipo específico (por ejemplo, una carpeta "Mis listas de reproducción" para listas de reproducción). Cada dispositivo tiene un sistema de archivos único y tendrá que decidir un lugar adecuado para buscar o enviar un archivo específico.

> [!Note]  
> Windows El Explorador puede mostrar carpetas virtuales que no existen realmente en el dispositivo. Las carpetas virtuales de ejemplo son las carpetas "Multimedia" y "Datos" que se muestran para los dispositivos MTP. Estas carpetas se crean mediante Windows para que las descargas sean más sencillas para los usuarios finales. no existen realmente en el dispositivo. La aplicación no debe depender de la búsqueda de estos tipos de carpetas generales. Por el contrario, Windows explorer podría no mostrar algunas carpetas u objetos que existen en el dispositivo (por ejemplo, listas de reproducción).

 

El siguiente código de ejemplo de C++ muestra la exploración recursiva de un dispositivo. Usa dos funciones:

-   ExploreDevice, una función inicial que recibe un puntero de dispositivo y obtiene un puntero al enumerador raíz de ese dispositivo.
-   RecursiveExploreStorage, al que se llama para explorar un dispositivo de forma recursiva.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




