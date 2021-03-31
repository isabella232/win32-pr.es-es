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
# <a name="exploring-a-device"></a><span data-ttu-id="82a27-110">Exploración de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="82a27-110">Exploring a Device</span></span>

<span data-ttu-id="82a27-111">La exploración de un dispositivo es similar a la exploración de una unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="82a27-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="82a27-112">Todos los objetos de un dispositivo se denominan *almacenamientos*.</span><span class="sxs-lookup"><span data-stu-id="82a27-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="82a27-113">Un almacenamiento puede ser un archivo, una carpeta o un objeto abstracto (como una lista de reproducción) en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82a27-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="82a27-114">Debe examinar los atributos y metadatos de un almacenamiento (si se admiten) para comprender qué tipo de almacenamiento es.</span><span class="sxs-lookup"><span data-stu-id="82a27-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="82a27-115">Los almacenamientos se organizan jerárquicamente en el dispositivo; cada almacenamiento tiene exactamente un elemento primario y todos los almacenamientos en última instancia descienden de un almacenamiento de dispositivo raíz único, normalmente denominado " \\ ".</span><span class="sxs-lookup"><span data-stu-id="82a27-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="82a27-116">En los pasos siguientes se describe cómo explorar un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="82a27-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="82a27-117">Obtiene la interfaz [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) de un dispositivo, tal y como se describe en [enumerar dispositivos](enumerating-devices.md).</span><span class="sxs-lookup"><span data-stu-id="82a27-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="82a27-118">Llame a [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) para recuperar una interfaz [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="82a27-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="82a27-119">Esta interfaz se usa para obtener todos los objetos secundarios del almacenamiento que devuelve esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="82a27-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="82a27-120">Al obtener esta interfaz desde el dispositivo, como estamos aquí, solo contendrá un almacenamiento: el almacenamiento del dispositivo raíz.</span><span class="sxs-lookup"><span data-stu-id="82a27-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="82a27-121">Llame a [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) con un recuento de 1 para recuperar la interfaz [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) para el almacenamiento del dispositivo raíz.</span><span class="sxs-lookup"><span data-stu-id="82a27-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="82a27-122">(No se puede solicitar más de un elemento secundario del dispositivo).</span><span class="sxs-lookup"><span data-stu-id="82a27-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="82a27-123">Examine todos los almacenamientos del dispositivo mediante una llamada recursiva a [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) y luego **IWMDMEnumStorage:: Next** para obtener elementos secundarios de un almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="82a27-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="82a27-124">Para ver si un almacenamiento tiene elementos secundarios para evitar las llamadas a **EnumStorage** y **Next**, puede llamar a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para comprobar las marcas que el atributo de almacenamiento de WMDM de WMDM \_ \_ \_ tiene \_ archivos o el atributo de almacenamiento de WMDM \_ \_ \_ tiene \_ carpetas.</span><span class="sxs-lookup"><span data-stu-id="82a27-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="82a27-125">Para obtener más información sobre cómo obtener las propiedades de un almacenamiento, vea [obtener y establecer metadatos y atributos](getting-and-setting-metadata-and-attributes.md) , y [obtener y establecer metadatos y atributos en la aplicación](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="82a27-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="82a27-126">Windows Media Administrador de dispositivos no expone un conjunto estándar de carpetas para almacenar los medios de un tipo específico (por ejemplo, una carpeta "mis listas de reproducción" para listas de reproducción).</span><span class="sxs-lookup"><span data-stu-id="82a27-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="82a27-127">Cada dispositivo tiene un sistema de archivos único y tendrá que decidir en un lugar adecuado para buscar, o enviar, un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="82a27-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="82a27-128">El explorador de Windows puede mostrar las carpetas virtuales que no existen realmente en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82a27-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="82a27-129">Las carpetas virtuales de ejemplo son las carpetas "multimedia" y "datos" que se muestran en los dispositivos MTP.</span><span class="sxs-lookup"><span data-stu-id="82a27-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="82a27-130">Windows crea estas carpetas para que las descargas resulten más sencillas para los usuarios finales. en realidad, no existen en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82a27-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="82a27-131">La aplicación no debe depender de la búsqueda de estos tipos de carpetas generales.</span><span class="sxs-lookup"><span data-stu-id="82a27-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="82a27-132">Por el contrario, es posible que el explorador de Windows no muestre algunas carpetas u objetos que existan en el dispositivo (por ejemplo, listas de reproducción).</span><span class="sxs-lookup"><span data-stu-id="82a27-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="82a27-133">En el código de ejemplo de C++ siguiente se muestra la exploración recursiva de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82a27-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="82a27-134">Usa dos funciones:</span><span class="sxs-lookup"><span data-stu-id="82a27-134">It uses two functions:</span></span>

-   <span data-ttu-id="82a27-135">ExploreDevice, una función de inicio que recibe un puntero de dispositivo y obtiene un puntero al enumerador raíz para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82a27-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="82a27-136">RecursiveExploreStorage, al que se llama para explorar un dispositivo de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="82a27-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82a27-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82a27-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a27-138">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="82a27-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




