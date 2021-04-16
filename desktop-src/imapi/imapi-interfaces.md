---
title: Interfaces de IMAPi
description: En las tablas siguientes se identifican y describen brevemente las interfaces utilizadas por los desarrolladores de C/C++ y el objeto de scripting asociado. Anteponga el nombre de objeto de la tabla con \ 0034; IMAPI2. \ 0034; para completar el nombre del objeto al crear el objeto en el script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105685672"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="5d2a8-105">Interfaces de IMAPi</span><span class="sxs-lookup"><span data-stu-id="5d2a8-105">IMAPI Interfaces</span></span>

<span data-ttu-id="5d2a8-106">En las tablas siguientes se identifican y describen brevemente las interfaces utilizadas por los desarrolladores de C/C++ y el objeto de scripting asociado.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="5d2a8-107">Anteponga el nombre del objeto en la tabla con "IMAPI2".</span><span class="sxs-lookup"><span data-stu-id="5d2a8-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="5d2a8-108">para completar el nombre del objeto al crear el objeto en el script.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="5d2a8-109">En la tabla siguiente se enumeran las interfaces asociadas a los dispositivos, el motor de grabación y el formato escritores y borrador.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d2a8-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="5d2a8-110">Interface</span></span></td>
<td><span data-ttu-id="5d2a8-111">Object</span><span class="sxs-lookup"><span data-stu-id="5d2a8-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-112">Motor de grabación de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="5d2a8-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-117">Escritor de imagen principal.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="5d2a8-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-122">Borrador de disco.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="5d2a8-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-126">Escritor de imágenes sin formato.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="5d2a8-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-131">Escritor de imágenes de un momento dado.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="5d2a8-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-136">Enumeración de los dispositivos de disco de la lista de hardware del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="5d2a8-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-139">Delegado de notificación para el objeto MsftDiscMaster2.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="5d2a8-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-142">Dispositivo de grabación individual.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="5d2a8-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-146">Atributos de escritura de dispositivos, incluido el tipo de medio, la velocidad de escritura y el tipo de control de velocidad angular.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-148">MsftWriteSpeedDescriptor</span><span class="sxs-lookup"><span data-stu-id="5d2a8-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5d2a8-149">En la tabla siguiente se enumeran las interfaces del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d2a8-150">Interfaz</span><span class="sxs-lookup"><span data-stu-id="5d2a8-150">Interface</span></span></td>
<td><span data-ttu-id="5d2a8-151">Object</span><span class="sxs-lookup"><span data-stu-id="5d2a8-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-152">Secuencia de imagen de arranque y propiedades para integrar la imagen de arranque en la imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-154">BootOptions</span><span class="sxs-lookup"><span data-stu-id="5d2a8-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-155">Imagen y propiedades del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-155">File system image and properties.</span></span> <span data-ttu-id="5d2a8-156">Este objeto incluye todas las pistas y referencias a la imagen de arranque y la imagen de resultado.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-162">CFileSystemImage</span><span class="sxs-lookup"><span data-stu-id="5d2a8-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-163">Contenedor del flujo de datos proporcionado por el objeto del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-165">FileSystemImageResult</span><span class="sxs-lookup"><span data-stu-id="5d2a8-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-166">Elemento de directorio de la imagen del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-169">FsiDirectoryItem</span><span class="sxs-lookup"><span data-stu-id="5d2a8-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-170">Elemento de archivo de la imagen del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-173">FsiFileItem</span><span class="sxs-lookup"><span data-stu-id="5d2a8-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-174">Interfaz que contiene propiedades comunes a los elementos de archivo y de directorio.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-176">FsiItem</span><span class="sxs-lookup"><span data-stu-id="5d2a8-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-177">Creación de imagen de CD sin formato.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-180">MsftRawCDImageCreator</span><span class="sxs-lookup"><span data-stu-id="5d2a8-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-181">Objeto auxiliar de objeto de secuencia para concatenar varias secuencias.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-183">MsftStreamConcatenate</span><span class="sxs-lookup"><span data-stu-id="5d2a8-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-184">Flujo intercalado que se va a agregar a la imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-186">MsftStreamInterleave</span><span class="sxs-lookup"><span data-stu-id="5d2a8-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-187">Secuencia generada pseudoaleatorios.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="5d2a8-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-190">El objeto de scripting <strong>MsftStreamZero</strong> no se implementa como una interfaz.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="5d2a8-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5d2a8-192">En la tabla siguiente se enumeran las interfaces auxiliares.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5d2a8-193">Interfaz</span><span class="sxs-lookup"><span data-stu-id="5d2a8-193">Interface</span></span></td>
<td><span data-ttu-id="5d2a8-194">Object</span><span class="sxs-lookup"><span data-stu-id="5d2a8-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-195">Colección de intervalos de sectores dentro de una imagen de sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-198">Ningún objeto correspondiente</span><span class="sxs-lookup"><span data-stu-id="5d2a8-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-199">Compatibilidad con la comprobación de la grabación.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-201">Ningún objeto correspondiente</span><span class="sxs-lookup"><span data-stu-id="5d2a8-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-202">Enumerador de FsiItems para las aplicaciones de C/C++.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-204">EnumFsiItems</span><span class="sxs-lookup"><span data-stu-id="5d2a8-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-205">Enumerador de ProgressItems para las aplicaciones de C/C++.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-207">EnumProgressItems</span><span class="sxs-lookup"><span data-stu-id="5d2a8-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="5d2a8-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="5d2a8-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-210">compatibilidad con la comprobación de imágenes. ISO.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-212">Ningún objeto correspondiente</span><span class="sxs-lookup"><span data-stu-id="5d2a8-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-213">Compatibilidad con varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-215">Ningún objeto correspondiente</span><span class="sxs-lookup"><span data-stu-id="5d2a8-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-216">Compatibilidad con varias sesiones secuenciales.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="5d2a8-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-219">MsftMultisessionSequential</span><span class="sxs-lookup"><span data-stu-id="5d2a8-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5d2a8-220">Nombre de archivo y bloques asociados en la imagen de resultado.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-222">ProgressItem</span><span class="sxs-lookup"><span data-stu-id="5d2a8-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5d2a8-223">Lista de imágenes de resultados, desglosadas por nombre de archivo y por bloques asociados.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="5d2a8-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="5d2a8-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="5d2a8-225">ProgressItems</span><span class="sxs-lookup"><span data-stu-id="5d2a8-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




