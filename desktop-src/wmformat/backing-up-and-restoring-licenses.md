---
title: Copia de seguridad y restauración de licencias
description: Copia de seguridad y restauración de licencias
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- SDK de Windows Media Format, copia de seguridad de licencias
- SDK de Windows Media Format, restaurar licencias
- SDK de Windows Media Format, copia de seguridad y restauración de licencias
- Advanced Systems Format (ASF), copia de seguridad de licencias
- ASF (formato de sistemas avanzados), copia de seguridad de licencias
- Advanced Systems Format (ASF), restaurar licencias
- ASF (formato de sistemas avanzados), restaurar licencias
- Formato de sistemas avanzados (ASF), copia de seguridad y restauración de licencias
- ASF (formato de sistemas avanzados), copia de seguridad y restauración de licencias
- Administración de derechos digitales (DRM), copia de seguridad de licencias
- DRM (administración de derechos digitales), copia de seguridad de licencias
- Administración de derechos digitales (DRM), restaurar licencias
- DRM (administración de derechos digitales), restaurar licencias
- Administración de derechos digitales (DRM), copia de seguridad y restauración de licencias
- DRM (administración de derechos digitales), copia de seguridad y restauración de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788787"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="1ba88-118">Copia de seguridad y restauración de licencias</span><span class="sxs-lookup"><span data-stu-id="1ba88-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="1ba88-119">Los procesos de copia de seguridad y restauración son asíncronos.</span><span class="sxs-lookup"><span data-stu-id="1ba88-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="1ba88-120">Se desencadenan cuando el usuario selecciona un comando de menú u opción en la aplicación para realizar una copia de seguridad o restaurar licencias.</span><span class="sxs-lookup"><span data-stu-id="1ba88-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="1ba88-121">Debe permitir que el usuario especifique las ubicaciones en las que se debe realizar una copia de seguridad de las licencias y restaurarlas desde.</span><span class="sxs-lookup"><span data-stu-id="1ba88-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="1ba88-122">Para realizar una copia de seguridad de las licencias:</span><span class="sxs-lookup"><span data-stu-id="1ba88-122">To back up licenses:</span></span>

1.  <span data-ttu-id="1ba88-123">Utilice la función [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) para crear el objeto de almacén de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1ba88-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="1ba88-124">Llame al método [**IWMBackupRestoreProps:: SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) para establecer la ruta de acceso de copia de seguridad (la ubicación donde escribirá los archivos, como un: \\ o D: \\ licenses).</span><span class="sxs-lookup"><span data-stu-id="1ba88-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="1ba88-125">Llame al método [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) para realizar una copia de seguridad de las licencias en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="1ba88-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="1ba88-126">Los eventos siguientes se envían al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="1ba88-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="1ba88-127">**WMT \_ BACKUPRESTORE \_ Begin** indica que se ha iniciado el proceso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1ba88-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="1ba88-128">**WMT \_ BACKUPRESTORE \_ End** indica que se ha completado el proceso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1ba88-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="1ba88-129">**WMT \_ \_Licencia restringida** indica que no se puede realizar una copia de seguridad de una o varias licencias porque el propietario del contenido no lo ha permitido.</span><span class="sxs-lookup"><span data-stu-id="1ba88-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="1ba88-130">El identificador de clave también se incluye en este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ba88-130">The key ID is also included in this message.</span></span> <span data-ttu-id="1ba88-131">Si ha implementado una base de datos para archivos protegidos que incluye el identificador y los metadatos de la clave, puede mostrar un mensaje al usuario con el título específico (por ejemplo, un título de la canción) para el que no se puede hacer una copia de seguridad de la licencia.</span><span class="sxs-lookup"><span data-stu-id="1ba88-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="1ba88-132">De lo contrario, el mensaje debe ser genérico e informar al usuario de que no se puede realizar una copia de seguridad de algunas licencias.</span><span class="sxs-lookup"><span data-stu-id="1ba88-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="1ba88-133">Para restaurar licencias:</span><span class="sxs-lookup"><span data-stu-id="1ba88-133">To restore licenses:</span></span>

1.  <span data-ttu-id="1ba88-134">Utilice la función **WMCreateBackupRestorer** para crear el objeto de almacén de copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1ba88-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="1ba88-135">Llame al método **IWMBackupRestoreProps:: SetProp** para establecer la ruta de acceso de restauración en la ubicación donde se realiza la copia de seguridad de las licencias.</span><span class="sxs-lookup"><span data-stu-id="1ba88-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="1ba88-136">Llame al método [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) para restaurar licencias desde esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="1ba88-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="1ba88-137">Los eventos siguientes se envían al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="1ba88-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="1ba88-138">**WMT \_ La \_ conexión de BACKUPRESTORE** indica que la aplicación se está conectando al servicio de administración de licencias.</span><span class="sxs-lookup"><span data-stu-id="1ba88-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="1ba88-139">**WMT \_ La \_ desconexión de BACKUPRESTORE** indica que la aplicación se está desconectando del servicio de administración de licencias.</span><span class="sxs-lookup"><span data-stu-id="1ba88-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="1ba88-140">**WMT \_ BACKUPRESTORE \_ Begin** indica que se ha iniciado el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="1ba88-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="1ba88-141">**WMT \_ BACKUPRESTORE \_ End** indica que se ha completado el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="1ba88-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="1ba88-142">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="1ba88-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1ba88-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ba88-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba88-144">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="1ba88-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1ba88-145">**Interfaz IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="1ba88-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="1ba88-146">**Interfaz IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="1ba88-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="1ba88-147">**Interfaz IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="1ba88-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




