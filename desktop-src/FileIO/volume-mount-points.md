---
description: Mediante el uso de carpetas montadas, puede unificar sistemas de archivos dispares como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un solo volumen NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Carpetas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687789"
---
# <a name="mounted-folders"></a><span data-ttu-id="84da8-103">Carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="84da8-103">Mounted Folders</span></span>

<span data-ttu-id="84da8-104">El sistema de archivos NTFS admite carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="84da8-104">The NTFS file system supports mounted folders.</span></span> <span data-ttu-id="84da8-105">Una *carpeta montada* es una asociación entre un volumen y un directorio de otro volumen.</span><span class="sxs-lookup"><span data-stu-id="84da8-105">A *mounted folder* is an association between a volume and a directory on another volume.</span></span> <span data-ttu-id="84da8-106">Cuando se crea una carpeta montada, los usuarios y las aplicaciones pueden acceder al volumen de destino mediante la ruta de acceso a la carpeta montada o mediante la letra de unidad del volumen.</span><span class="sxs-lookup"><span data-stu-id="84da8-106">When a mounted folder is created, users and applications can access the target volume either by using the path to the mounted folder or by using the volume's drive letter.</span></span> <span data-ttu-id="84da8-107">Por ejemplo, un usuario puede crear una carpeta montada para asociar la unidad D: a la carpeta C: \\ mnt \\ DDrive de la unidad c. Después de crear la carpeta montada, el usuario puede usar la ruta de acceso "C: \\ mnt \\ DDrive" para acceder a la unidad D: como si fuera una carpeta en la unidad C:.</span><span class="sxs-lookup"><span data-stu-id="84da8-107">For example, a user can create a mounted folder to associate drive D: with the C:\\Mnt\\DDrive folder on drive C. After creating the mounted folder, the user can use the "C:\\Mnt\\DDrive" path to access drive D: as if it were a folder on drive C:.</span></span>

<span data-ttu-id="84da8-108">Mediante el uso de carpetas montadas, puede unificar sistemas de archivos dispares como el sistema de archivos NTFS, un sistema de archivos FAT de 16 bits y un sistema de archivos ISO-9660 en una unidad de CD-ROM en un solo volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="84da8-108">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span> <span data-ttu-id="84da8-109">Ni los usuarios ni las aplicaciones necesitan información sobre el volumen de destino en el que se encuentra un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="84da8-109">Neither users nor applications need information about the target volume on which a specific file is located.</span></span> <span data-ttu-id="84da8-110">Toda la información que necesitan para localizar un archivo específico es una ruta de acceso completa que usa una carpeta montada en el volumen NTFS.</span><span class="sxs-lookup"><span data-stu-id="84da8-110">All the information they need to locate a specified file is a complete path using a mounted folder on the NTFS volume.</span></span> <span data-ttu-id="84da8-111">Los volúmenes se pueden reorganizar, sustituir o subdividir en muchos volúmenes sin necesidad de que los usuarios o las aplicaciones cambien la configuración.</span><span class="sxs-lookup"><span data-stu-id="84da8-111">Volumes can be rearranged, substituted, or subdivided into many volumes without users or applications needing to change settings.</span></span>

<span data-ttu-id="84da8-112">Para obtener información sobre las carpetas montadas, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="84da8-112">For information on mounted folders, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84da8-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="84da8-113">In this section</span></span>



| <span data-ttu-id="84da8-114">Tema</span><span class="sxs-lookup"><span data-stu-id="84da8-114">Topic</span></span>                                                                                                                         | <span data-ttu-id="84da8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="84da8-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84da8-116">Crear carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="84da8-116">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)<br/>                                                  | <span data-ttu-id="84da8-117">La creación de una carpeta montada es un proceso de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="84da8-117">Creating a mounted folder is a two-step process.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="84da8-118">Enumerar carpetas montadas</span><span class="sxs-lookup"><span data-stu-id="84da8-118">Enumerating Mounted Folders</span></span>](enumerating-volume-mount-points.md)<br/>                                                 | <span data-ttu-id="84da8-119">Funciones que se usan para enumerar las carpetas montadas en un volumen.</span><span class="sxs-lookup"><span data-stu-id="84da8-119">Functions to use to enumerate mounted folders on a volume.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="84da8-120">Determinar si un directorio es una carpeta montada</span><span class="sxs-lookup"><span data-stu-id="84da8-120">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | <span data-ttu-id="84da8-121">Cómo determinar si un directorio especificado es una carpeta montada.</span><span class="sxs-lookup"><span data-stu-id="84da8-121">How to determine whether a specified directory is a mounted folder.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="84da8-122">Asignación de una letra de unidad a un volumen</span><span class="sxs-lookup"><span data-stu-id="84da8-122">Assigning a Drive Letter to a Volume</span></span>](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | <span data-ttu-id="84da8-123">Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , siempre que no haya ningún volumen ya asignado a esa letra de unidad).</span><span class="sxs-lookup"><span data-stu-id="84da8-123">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span><br/> |
| [<span data-ttu-id="84da8-124">Funciones de carpeta montada</span><span class="sxs-lookup"><span data-stu-id="84da8-124">Mounted Folder Functions</span></span>](volume-mount-point-functions.md)<br/>                                                       | <span data-ttu-id="84da8-125">Funciones que se usan para administrar carpetas montadas.</span><span class="sxs-lookup"><span data-stu-id="84da8-125">Functions used to manage mounted folders.</span></span><br/>                                                                                                                                                                        |



 

<span data-ttu-id="84da8-126">Para obtener ejemplos, vea [ejemplos de carpeta montada](volume-mount-point-examples.md).</span><span class="sxs-lookup"><span data-stu-id="84da8-126">For examples, see [Mounted Folder Examples](volume-mount-point-examples.md).</span></span>

 

 




