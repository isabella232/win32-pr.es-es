---
title: Acerca de la supervisión de carpetas
description: Acerca de la supervisión de carpetas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, supervisión de carpetas
- Modelo de objetos de Windows Media Player, supervisión de carpetas
- modelo de objetos, supervisión de carpetas
- Control ActiveX de Windows Media Player, supervisión de carpetas
- Control ActiveX, supervisión de carpetas
- Control ActiveX móvil de Windows Media Player, supervisión de carpetas
- Windows Media Player Mobile, supervisión de carpetas
- supervisión de carpetas
- carpetas de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420226"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="92b4f-112">Acerca de la supervisión de carpetas</span><span class="sxs-lookup"><span data-stu-id="92b4f-112">About Folder Monitoring</span></span>

<span data-ttu-id="92b4f-113">Windows Media Player puede supervisar carpetas que contienen archivos multimedia digitales y actualizar la biblioteca cuando se agregan o quitan archivos.</span><span class="sxs-lookup"><span data-stu-id="92b4f-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="92b4f-114">La interfaz [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) proporciona esta funcionalidad de supervisión de carpetas.</span><span class="sxs-lookup"><span data-stu-id="92b4f-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="92b4f-115">Para usar los servicios de supervisión de carpetas, debe crear el objeto de reproductor en un estado remoto.</span><span class="sxs-lookup"><span data-stu-id="92b4f-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="92b4f-116">Para obtener más información sobre la comunicación remota, vea [comunicación remota del control de Media Player de Windows](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="92b4f-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="92b4f-117">Después de crear una instancia remota del reproductor, obtenga un puntero a la interfaz **IWMPFolderMonitorServices** llamando a **QueryInterface** en la interfaz [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .</span><span class="sxs-lookup"><span data-stu-id="92b4f-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="92b4f-118">Windows Media Player mantiene una lista de carpetas que se están supervisando.</span><span class="sxs-lookup"><span data-stu-id="92b4f-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="92b4f-119">Para obtener una lista de las carpetas supervisadas, use los métodos [IWMPFolderMonitorServices:: get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) y [IWMPFolderMonitorServices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) .</span><span class="sxs-lookup"><span data-stu-id="92b4f-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="92b4f-120">Para agregar carpetas a la lista o quitarlas de la lista, use los métodos [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) y [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="92b4f-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="92b4f-121">**Iniciar un examen**</span><span class="sxs-lookup"><span data-stu-id="92b4f-121">**Starting a Scan**</span></span>

<span data-ttu-id="92b4f-122">La supervisión de carpetas suele ser un proceso en segundo plano que no necesita llamarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="92b4f-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="92b4f-123">Si desea examinar activamente una carpeta, llame a [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="92b4f-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="92b4f-124">Puede detener un examen en curso con el método [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .</span><span class="sxs-lookup"><span data-stu-id="92b4f-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="92b4f-125">**Recuperando el estado de supervisión de carpetas**</span><span class="sxs-lookup"><span data-stu-id="92b4f-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="92b4f-126">**IWMPFolderMonitorServices** proporciona funcionalidad para recuperar el estado del proceso de supervisión de carpetas.</span><span class="sxs-lookup"><span data-stu-id="92b4f-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="92b4f-127">El examen de carpetas se realiza en dos pasos.</span><span class="sxs-lookup"><span data-stu-id="92b4f-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="92b4f-128">En el primer paso, el reproductor examina las carpetas mencionadas en la lista de carpetas supervisadas de una en una y crea una lista de los archivos que se van a agregar a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="92b4f-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="92b4f-129">En el segundo paso, se recorre la lista de archivos y se agregan los archivos a la biblioteca, y también se quitan los elementos multimedia de la biblioteca cuyos archivos físicos correspondientes se han eliminado del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="92b4f-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="92b4f-130">El evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) se usa para notificar al programa cada vez que el jugador cambie a un nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="92b4f-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="92b4f-131">También puede recuperar el estado actual llamando a [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span><span class="sxs-lookup"><span data-stu-id="92b4f-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="92b4f-132">Cuando se inicia el primer paso, el valor de estado actual es wmpfssScanning.</span><span class="sxs-lookup"><span data-stu-id="92b4f-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="92b4f-133">Durante el segundo paso, el estado cambia a wmpfssUpdating.</span><span class="sxs-lookup"><span data-stu-id="92b4f-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="92b4f-134">Una vez finalizado el proceso, el estado cambia a wmpfssStopped.</span><span class="sxs-lookup"><span data-stu-id="92b4f-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="92b4f-135">Mientras el reproductor está examinando las carpetas supervisadas en el primer paso, llame a [Get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para comprobar el número de archivos que se han analizado.</span><span class="sxs-lookup"><span data-stu-id="92b4f-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="92b4f-136">El método [Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) le indicará qué carpeta se está analizando actualmente.</span><span class="sxs-lookup"><span data-stu-id="92b4f-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="92b4f-137">Una vez iniciada la segunda fase, llame a [Get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para comprobar el número de archivos que se han agregado a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="92b4f-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="92b4f-138">El método [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) le indicará el progreso del segundo paso, en forma de porcentaje de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="92b4f-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92b4f-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92b4f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b4f-140">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="92b4f-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="92b4f-141">**Interfaz IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="92b4f-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




