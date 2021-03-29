---
title: Grabación de una imagen de disco
description: La creación de patrones (grabación de un disco) mediante IMAPi consta de los pasos siguientes para crear una imagen de sistema de archivos que contiene los directorios y archivos que se van a escribir en el disco. Configure una grabadora de discos para comunicarse con el dispositivo óptico. Cree un escritor de datos y grabe la imagen en el disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358903"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="284d0-103">Grabación de una imagen de disco</span><span class="sxs-lookup"><span data-stu-id="284d0-103">Burning a Disc Image</span></span>

<span data-ttu-id="284d0-104">La maestra (grabación de un disco) mediante IMAPi consta de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="284d0-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="284d0-105">Construya una imagen del sistema de archivos que contenga los directorios y archivos para escribir el disco.</span><span class="sxs-lookup"><span data-stu-id="284d0-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="284d0-106">[Configure una grabadora de discos](#set-up-a-disc-recorder) para comunicarse con el dispositivo óptico.</span><span class="sxs-lookup"><span data-stu-id="284d0-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="284d0-107">[Cree un escritor de datos](#create-a-data-writer-and-write-the-burn-image) y grabe la imagen en el disco.</span><span class="sxs-lookup"><span data-stu-id="284d0-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="284d0-108">Para obtener un ejemplo en el que se grabe una imagen de disco, vea el [ejemplo de VBScript](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="284d0-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="284d0-109">Construir una imagen de grabación</span><span class="sxs-lookup"><span data-stu-id="284d0-109">Construct a burn image</span></span>

<span data-ttu-id="284d0-110">Una imagen de grabación es un flujo de datos que está listo para escribirse en un medio óptico.</span><span class="sxs-lookup"><span data-stu-id="284d0-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="284d0-111">La imagen de grabación para los formatos ISO9660, Joliet y UDF se compone de un sistema de archivos de archivos y directorios individuales.</span><span class="sxs-lookup"><span data-stu-id="284d0-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="284d0-112">El objeto **CFileSystemImage** es el objeto del sistema de archivos que contiene los archivos y directorios que se colocarán en los medios ópticos.</span><span class="sxs-lookup"><span data-stu-id="284d0-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="284d0-113">La interfaz [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) proporciona acceso al objeto y a la configuración del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="284d0-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="284d0-114">Después de crear el objeto del sistema de archivos, llame a los métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) y [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para crear los objetos de archivo y directorio, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="284d0-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="284d0-115">Los objetos de archivo y directorio se pueden usar para proporcionar detalles específicos sobre el archivo y el directorio.</span><span class="sxs-lookup"><span data-stu-id="284d0-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="284d0-116">Los métodos de control de eventos disponibles para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) pueden identificar el archivo actual que se está agregando a la imagen del sistema de archivos, el número de sectores ya copiados y el número total de sectores que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="284d0-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="284d0-117">Opcionalmente, se puede adjuntar una imagen de arranque al sistema de archivos mediante la propiedad [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) .</span><span class="sxs-lookup"><span data-stu-id="284d0-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="284d0-118">Para obtener un ejemplo, vea [Agregar una imagen de arranque](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="284d0-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="284d0-119">Por último, llame a [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para crear un flujo de datos y proporcionar acceso a través de [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="284d0-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="284d0-120">El nuevo flujo de datos se puede proporcionar directamente al método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o guardarse en un archivo para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="284d0-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="284d0-121">Configuración de una grabadora de discos</span><span class="sxs-lookup"><span data-stu-id="284d0-121">Set up a disc recorder</span></span>

<span data-ttu-id="284d0-122">El objeto **MsftDiscMaster2** proporciona una enumeración de los dispositivos ópticos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="284d0-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="284d0-123">La interfaz [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) proporciona acceso a la enumeración del dispositivo resultante.</span><span class="sxs-lookup"><span data-stu-id="284d0-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="284d0-124">Recorra las enumeraciones para buscar un dispositivo de grabación adecuado.</span><span class="sxs-lookup"><span data-stu-id="284d0-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="284d0-125">El objeto **MsftDiscMaster2** también proporciona notificaciones de eventos cuando se agregan o eliminan dispositivos ópticos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="284d0-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="284d0-126">Después de buscar una grabadora óptica y recuperar su identificador, cree un objeto **MsftDiscRecorder2** e inicialice la grabadora con el identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="284d0-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="284d0-127">La interfaz [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) proporciona acceso al objeto de grabadora, así como a información básica del dispositivo, como el identificador del proveedor, el ID. del producto, la revisión del producto y los métodos para expulsar el medio y cerrar la bandeja.</span><span class="sxs-lookup"><span data-stu-id="284d0-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="284d0-128">Creación de un escritor de datos y escritura de la imagen de grabación</span><span class="sxs-lookup"><span data-stu-id="284d0-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="284d0-129">El objeto **MsftDiscFormat2Data** proporciona el método de escritura, las propiedades de la función de escritura y las propiedades específicas de los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="284d0-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="284d0-130">La interfaz [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) proporciona acceso al objeto **MsftDiscFormat2Data** .</span><span class="sxs-lookup"><span data-stu-id="284d0-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="284d0-131">La grabadora de CD vincula al escritor de formato mediante la propiedad [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="284d0-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="284d0-132">Después de enlazar la grabadora al escritor de formato, puede realizar consultas sobre el medio y actualizar las propiedades específicas de la escritura antes de escribir la imagen resultante en el disco mediante el método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="284d0-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="284d0-133">Otras interfaces de escritura de formato proporcionadas por IMAPi funcionan de forma similar. entre las interfaces de escritura de formato adicionales se incluyen:</span><span class="sxs-lookup"><span data-stu-id="284d0-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="284d0-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) borra los medios ópticos regrabables.</span><span class="sxs-lookup"><span data-stu-id="284d0-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="284d0-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) escribe una imagen sin procesar en un medio óptico.</span><span class="sxs-lookup"><span data-stu-id="284d0-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="284d0-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) escribe pistas de audio en medios ópticos.</span><span class="sxs-lookup"><span data-stu-id="284d0-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="284d0-137">Es posible que se produzca una transición de estado de energía durante una operación de grabación (es decir, el cierre de sesión del usuario o la suspensión del sistema), lo que provoca la interrupción del proceso de grabación y la posible pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="284d0-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="284d0-138">Para conocer las consideraciones de programación, vea [evitar el cierre de sesión o la suspensión durante una grabación](preventing-logoff-or-suspend-during-a-burn.md).</span><span class="sxs-lookup"><span data-stu-id="284d0-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="284d0-139">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="284d0-139">VBScript example</span></span>

<span data-ttu-id="284d0-140">En este ejemplo de script se muestra cómo usar los objetos de IMAPi para grabar medios ópticos; más concretamente, escriba un directorio en un disco en blanco. El código no contiene ninguna comprobación de errores y asume lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="284d0-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="284d0-141">Un dispositivo de disco compatible está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="284d0-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="284d0-142">El dispositivo de disco es la segunda unidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="284d0-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="284d0-143">Se inserta un disco compatible en el dispositivo de disco.</span><span class="sxs-lookup"><span data-stu-id="284d0-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="284d0-144">El disco está en blanco.</span><span class="sxs-lookup"><span data-stu-id="284d0-144">The disc is blank.</span></span>
-   <span data-ttu-id="284d0-145">Los archivos que se van a escribir en el disco se encuentran en "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="284d0-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="284d0-146">Puede agregarse a este script una funcionalidad adicional, como la comprobación de errores, la compatibilidad de dispositivos y medios, la notificación de eventos y el cálculo del espacio libre en el disco.</span><span class="sxs-lookup"><span data-stu-id="284d0-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="284d0-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="284d0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="284d0-148">Usar IMAPi</span><span class="sxs-lookup"><span data-stu-id="284d0-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="284d0-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="284d0-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="284d0-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="284d0-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="284d0-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="284d0-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="284d0-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="284d0-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="284d0-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="284d0-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="284d0-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="284d0-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="284d0-155">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="284d0-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="284d0-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="284d0-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 