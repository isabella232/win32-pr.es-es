---
title: Exploración de un dispositivo
description: Exploración de un dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Administrador de dispositivos, explorar dispositivos
- Administrador de dispositivos, explorar dispositivos
- Guía de programación, explorar dispositivos
- aplicaciones de escritorio, explorar dispositivos
- crear aplicaciones de Windows Media Administrador de dispositivos, explorar dispositivos
- exploración de dispositivos
- almacenamientos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418741"
---
# <a name="exploring-a-device"></a>Exploración de un dispositivo

La exploración de un dispositivo es similar a la exploración de una unidad de disco. Todos los objetos de un dispositivo se denominan *almacenamientos*. Un almacenamiento puede ser un archivo, una carpeta o un objeto abstracto (como una lista de reproducción) en el dispositivo. Debe examinar los atributos y metadatos de un almacenamiento (si se admiten) para comprender qué tipo de almacenamiento es. Los almacenamientos se organizan jerárquicamente en el dispositivo; cada almacenamiento tiene exactamente un elemento primario y todos los almacenamientos en última instancia descienden de un almacenamiento de dispositivo raíz único, normalmente denominado " \\ ".

En los pasos siguientes se describe cómo explorar un dispositivo:

1.  Obtiene la interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) de un dispositivo, tal y como se describe en [enumerar dispositivos](enumerating-devices.md).
2.  Llame a [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) para recuperar una interfaz [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) . Esta interfaz se usa para obtener todos los objetos secundarios del almacenamiento que devuelve esta interfaz. Al obtener esta interfaz desde el dispositivo, como estamos aquí, solo contendrá un almacenamiento: el almacenamiento del dispositivo raíz.
3.  Llame a [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) con un recuento de 1 para recuperar la interfaz [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) para el almacenamiento del dispositivo raíz. (No se puede solicitar más de un elemento secundario del dispositivo).
4.  Examine todos los almacenamientos del dispositivo mediante una llamada recursiva a [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) y luego **IWMDMEnumStorage:: Next** para obtener elementos secundarios de un almacenamiento. Para ver si un almacenamiento tiene elementos secundarios para evitar las llamadas a **EnumStorage** y **Next**, puede llamar a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para comprobar las marcas que el atributo de almacenamiento de WMDM de WMDM \_ \_ \_ tiene \_ archivos o el atributo de almacenamiento de WMDM \_ \_ \_ tiene \_ carpetas. Para obtener más información sobre cómo obtener las propiedades de un almacenamiento, vea [obtener y establecer metadatos y atributos](getting-and-setting-metadata-and-attributes.md) , y [obtener y establecer metadatos y atributos en la aplicación](getting-and-setting-metadata-and-attributes-in-the-application.md).

Windows Media Administrador de dispositivos no expone un conjunto estándar de carpetas para almacenar los medios de un tipo específico (por ejemplo, una carpeta "mis listas de reproducción" para listas de reproducción). Cada dispositivo tiene un sistema de archivos único y tendrá que decidir en un lugar adecuado para buscar, o enviar, un archivo específico.

> [!Note]  
> El explorador de Windows puede mostrar las carpetas virtuales que no existen realmente en el dispositivo. Las carpetas virtuales de ejemplo son las carpetas "multimedia" y "datos" que se muestran en los dispositivos MTP. Windows crea estas carpetas para que las descargas resulten más sencillas para los usuarios finales. en realidad, no existen en el dispositivo. La aplicación no debe depender de la búsqueda de estos tipos de carpetas generales. Por el contrario, es posible que el explorador de Windows no muestre algunas carpetas u objetos que existan en el dispositivo (por ejemplo, listas de reproducción).

 

En el código de ejemplo de C++ siguiente se muestra la exploración recursiva de un dispositivo. Usa dos funciones:

-   ExploreDevice, una función de inicio que recibe un puntero de dispositivo y obtiene un puntero al enumerador raíz para ese dispositivo.
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

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




