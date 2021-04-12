---
title: Asignación previa de espacio en disco para el archivo de captura
description: Asignación previa de espacio en disco para el archivo de captura
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Mensaje WM_CAP_FILE_ALLOCATE
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357010"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="cc3bc-105">Asignación previa de espacio en disco para el archivo de captura</span><span class="sxs-lookup"><span data-stu-id="cc3bc-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="cc3bc-106">La asignación previa de espacio en disco para el archivo de captura crea un archivo de un tamaño especificado en el disco antes del inicio de una operación de captura.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="cc3bc-107">La asignación previa de un archivo de captura reduce el procesamiento necesario mientras la captura está en curso y da lugar a menos fotogramas quitados.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="cc3bc-108">Puede preasignar un archivo de captura mediante el mensaje [**de \_ \_ \_ asignación de archivo Cap de WM**](wm-cap-file-allocate.md) (o la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).</span><span class="sxs-lookup"><span data-stu-id="cc3bc-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="cc3bc-109">Normalmente, la aplicación debe preasignar suficiente espacio en disco para contener el archivo de captura más grande previsto.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="cc3bc-110">La asignación previa de espacio en disco no restringe el tamaño del archivo capturado.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="cc3bc-111">El tamaño del archivo se amplía automáticamente si los datos capturados superan el espacio asignado.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="cc3bc-112">Las operaciones de escritura posteriores en el archivo de captura reutilizan las partes de espacio en disco asignadas para el archivo, conservando el tamaño y la fragmentación del archivo.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="cc3bc-113">También puede mejorar el rendimiento de la captura desfragmentando el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="cc3bc-114">Para desfragmentar el archivo, use una utilidad de desfragmentación como Desfragmentador de disco.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="cc3bc-115">Si utiliza un archivo de captura desfragmentado y más adelante lo amplía, debe desfragmentar el archivo de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="cc3bc-116">La ampliación de un archivo de captura desfragmentado puede fragmentar la parte expandida del archivo y reducir el rendimiento en la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="cc3bc-117">También puede mejorar el rendimiento mediante el uso de un disco sin comprimir para la captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="cc3bc-118">La compresión de datos durante la captura puede limitar el rendimiento de la captura en el disco.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="cc3bc-119">Una aplicación puede reservar un archivo de captura permanente para eliminar el tiempo necesario para preasignar y desfragmentar un archivo cada vez que se inicia.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="cc3bc-120">Dado que un archivo de captura puede requerir un gran espacio en disco y la asignación previa de un archivo de captura quita todos los datos de un archivo de captura existente, una aplicación debe permitir que el usuario decida si el archivo es permanente o temporal.</span><span class="sxs-lookup"><span data-stu-id="cc3bc-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




