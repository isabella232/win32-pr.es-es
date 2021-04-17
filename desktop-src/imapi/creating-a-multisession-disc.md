---
title: Creación de un disco de múltiples sesiones
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: Más información acerca de cómo crear un disco de varias sesiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497830"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="30ca2-103">Creación de un disco de múltiples sesiones</span><span class="sxs-lookup"><span data-stu-id="30ca2-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="30ca2-104">La [API de procesamiento de imágenes](about-imapi.md) (IMAPI) admite la adición y eliminación de archivos a los siguientes tipos de discos de múltiples sesiones:</span><span class="sxs-lookup"><span data-stu-id="30ca2-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="30ca2-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="30ca2-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="30ca2-106">Single-Layer DVD + R/DVD-R</span><span class="sxs-lookup"><span data-stu-id="30ca2-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="30ca2-107">DVD + R capa dual</span><span class="sxs-lookup"><span data-stu-id="30ca2-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="30ca2-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="30ca2-108">BD-R</span></span>
-   <span data-ttu-id="30ca2-109">DVD-RW/DVD + RW (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="30ca2-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="30ca2-110">DVD-RAM (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="30ca2-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="30ca2-111">BD-RE (**solo Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="30ca2-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="30ca2-112">La creación de un disco de múltiples sesiones con IMAPi consta de los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="30ca2-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="30ca2-113">Cada uno de estos pasos documentados contiene la parte correspondiente del ejemplo de script completo Visual Basic proporcionado en la sección final.</span><span class="sxs-lookup"><span data-stu-id="30ca2-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="30ca2-114">Inicializando la grabadora de discos</span><span class="sxs-lookup"><span data-stu-id="30ca2-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="30ca2-115">Antes de la inicialización del dispositivo, el objeto **MsftDiscMaster2** proporciona una enumeración de los dispositivos ópticos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="30ca2-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="30ca2-116">La interfaz [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) proporciona acceso a esta enumeración de dispositivos para facilitar la ubicación del dispositivo de grabación adecuado.</span><span class="sxs-lookup"><span data-stu-id="30ca2-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="30ca2-117">El objeto **MsftDiscMaster2** también proporciona notificaciones de eventos cuando se agregan o se quitan dispositivos ópticos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="30ca2-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="30ca2-118">Después de localizar un grabador óptico y recuperar el identificador asignado a él, cree un nuevo objeto **MsftDiscMaster2** e inicialice la grabadora con el identificador de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="30ca2-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="30ca2-119">La interfaz [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) proporciona acceso a información básica del dispositivo, como el identificador del proveedor, el ID. del producto, la revisión del producto, así como los métodos para expulsar el contenido multimedia o cerrar la bandeja.</span><span class="sxs-lookup"><span data-stu-id="30ca2-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="30ca2-120">Las constantes y dimensiones adicionales declaradas en el ejemplo siguiente se usan más adelante en el script de ejemplo completo que se encuentra en la sección final de este documento.</span><span class="sxs-lookup"><span data-stu-id="30ca2-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="30ca2-121">Estos elementos no son necesarios para la acción de inicializar una grabadora de discos.</span><span class="sxs-lookup"><span data-stu-id="30ca2-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="30ca2-122">Crear un escritor de datos</span><span class="sxs-lookup"><span data-stu-id="30ca2-122">Creating a Data Writer</span></span>

<span data-ttu-id="30ca2-123">El objeto _ *MsftDiscFormat2Data*\* proporciona el método de escritura, sus propiedades, así como las propiedades específicas del medio.</span><span class="sxs-lookup"><span data-stu-id="30ca2-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="30ca2-124">La interfaz [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) proporciona acceso a este objeto.</span><span class="sxs-lookup"><span data-stu-id="30ca2-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="30ca2-125">La grabadora de discos se enlaza al escritor de formato mediante la propiedad de [**\_ grabadora IDiscFormat2Data::p UT**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="30ca2-126">Después de que la grabadora esté enlazada al escritor de formato, se pueden realizar consultas de propiedades de medios y específicas de escritura antes de escribir la imagen de resultado en el disco mediante el método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="30ca2-127">La cadena de nombre de cliente especificada en el código de ejemplo siguiente debe ajustarse según corresponda para la aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="30ca2-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="30ca2-128">Crear el objeto del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="30ca2-128">Creating the File System Object</span></span>

<span data-ttu-id="30ca2-129">Para registrar una nueva sesión, debe generarse una imagen de grabación en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="30ca2-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="30ca2-130">Una imagen de grabación para los formatos de **ISO9660**, **Joliet** y **UDF** se compone de sistemas de archivos de archivos y directorios individuales.</span><span class="sxs-lookup"><span data-stu-id="30ca2-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="30ca2-131">El objeto **MsftFileSystemImage** es el objeto del sistema de archivos que contiene los archivos y directorios que se van a colocar en el medio óptico.</span><span class="sxs-lookup"><span data-stu-id="30ca2-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="30ca2-132">La interfaz [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) proporciona acceso al objeto y a la configuración del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="30ca2-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="30ca2-133">Importar un sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="30ca2-133">Importing a File System</span></span>

<span data-ttu-id="30ca2-134">Antes de continuar, asegúrese de que el disco no esté en blanco; para ello, Compruebe la propiedad [**IDiscFormat2:: get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="30ca2-135">Después de crear el objeto **MsftFileSystemImage** , la propiedad [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) debe inicializarse antes de una llamada al método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) o [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) para importar el sistema de archivos desde la última sesión grabada.</span><span class="sxs-lookup"><span data-stu-id="30ca2-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="30ca2-136">Estos métodos rellenarán automáticamente el objeto **MsftFileSystemImage** con información que describe los archivos y directorios grabados previamente.</span><span class="sxs-lookup"><span data-stu-id="30ca2-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="30ca2-137">La propiedad [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) se inicializa normalmente con las interfaces de sesión múltiples que proporciona el escritor de datos a través de la propiedad [**IDiscFormat2Data:: get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="30ca2-138">Si se intenta establecer la propiedad **IFileSystemImage::p UT \_ MultisessionInterfaces** , se producirá un error si IMAPI no admite la multisesión para los medios insertados actualmente o si los medios no se pueden anexar por algún otro motivo (por ejemplo, porque está cerrado).</span><span class="sxs-lookup"><span data-stu-id="30ca2-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="30ca2-139">Si la sesión de grabación anterior contenía más de un tipo de sistema de archivos, el método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importará información del tipo de sistema de archivos más avanzado presente.</span><span class="sxs-lookup"><span data-stu-id="30ca2-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="30ca2-140">Por ejemplo, en el ejemplo que se proporciona en este tema, UDF es el sistema de archivos importado.</span><span class="sxs-lookup"><span data-stu-id="30ca2-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="30ca2-141">Sin embargo, el uso del método [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permite la importación específica del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="30ca2-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="30ca2-142">El método [**IFileSystemImage:: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) se puede usar para determinar los sistemas de archivos que están disponibles en el disco.</span><span class="sxs-lookup"><span data-stu-id="30ca2-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="30ca2-143">Agregar o quitar archivos en el sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="30ca2-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="30ca2-144">Después de crear el objeto del sistema de archivos e importar el sistema de archivos de la sesión anterior, llame a los métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) y [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para crear nuevos objetos de archivo y directorio, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="30ca2-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="30ca2-145">Los objetos de archivo y directorio proporcionan detalles específicos sobre los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="30ca2-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="30ca2-146">Como alternativa, se puede usar el método [**IFsiDirectoryItem:: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) de un objeto de directorio, representado mediante la interfaz [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , para agregar archivos y directorios existentes desde otro dispositivo de almacenamiento (es decir, una unidad de disco duro).</span><span class="sxs-lookup"><span data-stu-id="30ca2-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="30ca2-147">El método de actualización del controlador de eventos disponible para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica el archivo actual que se está agregando a la imagen del sistema de archivos, el número de sectores ya copiados y el número total de sectores que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="30ca2-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="30ca2-148">Para quitar los archivos y directorios existentes del sistema de archivos, use los métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) y [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) de los objetos de directorio que se representan a través de la interfaz [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="30ca2-149">La propiedad [**IFileSystemImage:: get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) se usa para obtener un puntero al directorio raíz del sistema de archivos y la interfaz **IFsiDirectoryItem** para atravesar el árbol de directorios.</span><span class="sxs-lookup"><span data-stu-id="30ca2-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="30ca2-150">Los archivos y directorios que se quitan mediante los métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) y [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) no se quitan físicamente del disco y el software avanzado puede recuperar fácilmente la información eliminada.</span><span class="sxs-lookup"><span data-stu-id="30ca2-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="30ca2-151">Construir una imagen de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="30ca2-151">Constructing a File System Image</span></span>

<span data-ttu-id="30ca2-152">El paso final consiste en llamar a [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para crear un flujo de datos para la imagen de grabación y proporcionar acceso a él a través de la interfaz [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) .</span><span class="sxs-lookup"><span data-stu-id="30ca2-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="30ca2-153">Este flujo de datos se puede proporcionar directamente al método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o guardarse en un archivo para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="30ca2-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="30ca2-154">Resumen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="30ca2-154">Example Summary</span></span>

<span data-ttu-id="30ca2-155">En el siguiente ejemplo de script de Visual Basic se muestra cómo usar los objetos de IMAPi para crear discos de múltiples sesiones.</span><span class="sxs-lookup"><span data-stu-id="30ca2-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="30ca2-156">En el ejemplo se crea una nueva sesión y se agrega un directorio al disco. Por motivos de simplicidad, el código no realiza una comprobación de errores exhaustiva y presupone lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="30ca2-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="30ca2-157">Un dispositivo de disco compatible está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="30ca2-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="30ca2-158">El dispositivo de disco es la primera unidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="30ca2-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="30ca2-159">Se inserta un disco compatible en el dispositivo de disco.</span><span class="sxs-lookup"><span data-stu-id="30ca2-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="30ca2-160">Los archivos que se van a agregar al disco se encuentran en "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="30ca2-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="30ca2-161">Se puede Agregar al script una funcionalidad adicional, como la comprobación de errores, la compatibilidad de dispositivos y medios, la notificación de eventos y el cálculo del espacio libre en el disco.</span><span class="sxs-lookup"><span data-stu-id="30ca2-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="30ca2-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30ca2-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30ca2-163">Usar IMAPi</span><span class="sxs-lookup"><span data-stu-id="30ca2-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="30ca2-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="30ca2-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="30ca2-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="30ca2-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="30ca2-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="30ca2-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="30ca2-167">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="30ca2-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
