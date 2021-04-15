---
description: La creación de una carpeta montada es un proceso de dos pasos.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Crear carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688658"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="f7f4a-103">Crear carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="f7f4a-103">Creating Mounted Folders</span></span>

<span data-ttu-id="f7f4a-104">La creación de una carpeta montada es un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="f7f4a-105">En primer lugar, llame a [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con el punto de montaje (letra de unidad, ruta de acceso de GUID de volumen o carpeta montada) del volumen que se va a asignar a la carpeta montada.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="f7f4a-106">A continuación, utilice la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para asociar la ruta de acceso del GUID de volumen devuelta al directorio deseado en otro volumen.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="f7f4a-107">Para ver un ejemplo de código, vea [crear una carpeta montada](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="f7f4a-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="f7f4a-108">La aplicación puede designar cualquier directorio vacío en un volumen distinto de la raíz como una carpeta montada.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="f7f4a-109">Cuando se llama a la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , ese directorio se convierte en la carpeta montada.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="f7f4a-110">Puede asignar el mismo volumen a varias carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="f7f4a-111">Una vez establecida la carpeta montada, se mantiene a través de los reinicios del equipo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="f7f4a-112">Si se produce un error en un volumen, ya no se puede tener acceso a los volúmenes asignados a las carpetas montadas en ese volumen a través de esas carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="f7f4a-113">Por ejemplo, supongamos que tiene dos volúmenes, C: y D:, y que D: está asociado a la carpeta montada C: \\ montada \\ .</span><span class="sxs-lookup"><span data-stu-id="f7f4a-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="f7f4a-114">Si se produce un error en el volumen C:, ya no se puede acceder al volumen D: a través de la ruta de acceso C: \\ montada \\ .</span><span class="sxs-lookup"><span data-stu-id="f7f4a-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="f7f4a-115">Solo los volúmenes del sistema de archivos NTFS pueden tener carpetas montadas, pero los volúmenes de destino de las carpetas montadas pueden ser volúmenes que no son NTFS.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="f7f4a-116">Las carpetas montadas se implementan mediante puntos de análisis y están sujetas a sus restricciones.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="f7f4a-117">Para obtener más información, vea [puntos de reanálisis](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="f7f4a-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="f7f4a-118">No es necesario manipular los puntos de reanálisis para usar carpetas montadas; funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) controlan todos los detalles del punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="f7f4a-119">Dado que las carpetas montadas son directorios, puede cambiarles el nombre, quitarlas, moverlas y, de lo contrario, manipularlas, como haría con otros directorios.</span><span class="sxs-lookup"><span data-stu-id="f7f4a-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="f7f4a-120">(Nota: la documentación de TechNet usa el término *unidades montadas* para hacer referencia a *las carpetas montadas*).</span><span class="sxs-lookup"><span data-stu-id="f7f4a-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



