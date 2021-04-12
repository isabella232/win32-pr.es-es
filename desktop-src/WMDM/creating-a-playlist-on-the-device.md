---
title: Creación de una lista de reproducción en el dispositivo
description: Creación de una lista de reproducción en el dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Administrador de dispositivos, listas de reproducción
- Administrador de dispositivos, listas de reproducción
- Guía de programación, listas de reproducción
- aplicaciones de escritorio, listas de reproducción
- crear aplicaciones de Windows Media Administrador de dispositivos, listas de reproducción
- listas de reproducción abstractas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356969"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="07adc-109">Creación de una lista de reproducción en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="07adc-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="07adc-110">El SDK de Administrador de dispositivos de Windows Media proporciona los medios para que una aplicación MTP cree una lista de reproducción en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07adc-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="07adc-111">Este tipo de lista de reproducción se denomina lista de reproducción *abstracta* , ya que el archivo creado en el dispositivo no contiene datos multimedia, sino solo metadatos, que contienen los vínculos a archivos multimedia en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="07adc-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="07adc-112">Otros elementos abstractos que se pueden crear en el dispositivo son los álbumes (esencialmente listas de reproducción con propiedades adicionales como la cubierta), los contactos y los mensajes.</span><span class="sxs-lookup"><span data-stu-id="07adc-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="07adc-113">**Para crear una lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="07adc-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="07adc-114">Adquiera una interfaz [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="07adc-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="07adc-115">Llame a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obtener la \_ propiedad g wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="07adc-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="07adc-116">Si no se admiten formatos de lista de reproducción, no se permite el envío de listas de reproducción al dispositivo y se omiten los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="07adc-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="07adc-117">De lo contrario, elija el código de formato compatible con el dispositivo que coincida con el tipo de objeto previsto.</span><span class="sxs-lookup"><span data-stu-id="07adc-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="07adc-118">Los códigos de formato genérico de WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST y WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST son los que se admiten con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="07adc-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="07adc-119">Obtenga una interfaz [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para el almacenamiento (la raíz o una carpeta) en la que desea crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="07adc-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="07adc-120">Algunos dispositivos funcionan mejor si el objeto de lista de reproducción se coloca en una carpeta de nivel superior denominada "listas de reproducción".</span><span class="sxs-lookup"><span data-stu-id="07adc-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="07adc-121">Cree un objeto de metadatos vacío mediante [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="07adc-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="07adc-122">Con la interfaz **IWMDMMetaData** obtenida en el paso anterior, llame a [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para agregar el código de formato elegido (del paso 3) a las propiedades de los metadatos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="07adc-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="07adc-123">Obtenga la interfaz [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) de la interfaz **IWMDMStorage3** .</span><span class="sxs-lookup"><span data-stu-id="07adc-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="07adc-124">Llame a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para insertar un nuevo archivo de lista de reproducción en el almacenamiento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="07adc-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="07adc-125">Este archivo contiene los metadatos representados por la interfaz **IWMDMMetaData** que creó en el paso 5 y que se pasaron a **Insert3**.</span><span class="sxs-lookup"><span data-stu-id="07adc-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="07adc-126">El método devuelve una interfaz **IWMDMStorage** para el archivo de lista de reproducción; puede consultar la interfaz [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .</span><span class="sxs-lookup"><span data-stu-id="07adc-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="07adc-127">Llame a [**IWMDMStorage4:: SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para crear referencias a las interfaces **IWMDMStorage** de los archivos multimedia en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="07adc-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="07adc-128">Para ver un ejemplo de código, vea la \_ función OnCreatePlaylist en la [aplicación de escritorio de ejemplo](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="07adc-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="07adc-129">El proveedor de servicios MTP proporcionado por Microsoft permite a una aplicación establecer referencias en los metadatos.</span><span class="sxs-lookup"><span data-stu-id="07adc-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="07adc-130">Para implementar listas de reproducción, la aplicación debe comunicarse con un dispositivo MTP o con un proveedor de servicios personalizado que pueda administrar objetos abstractos.</span><span class="sxs-lookup"><span data-stu-id="07adc-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="07adc-131">El proveedor de servicios CE administra la lista de reproducción y los objetos de álbum.</span><span class="sxs-lookup"><span data-stu-id="07adc-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07adc-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07adc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07adc-133">**Escribir archivos en el dispositivo**</span><span class="sxs-lookup"><span data-stu-id="07adc-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




