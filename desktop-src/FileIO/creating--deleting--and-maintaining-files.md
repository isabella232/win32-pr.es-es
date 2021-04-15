---
description: Funciones que se van a usar para crear, eliminar y mantener archivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Crear, eliminar y mantener archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669698"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="722f0-103">Crear, eliminar y mantener archivos</span><span class="sxs-lookup"><span data-stu-id="722f0-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="722f0-104">En los temas siguientes se describe cómo crear, eliminar y mantener archivos.</span><span class="sxs-lookup"><span data-stu-id="722f0-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="722f0-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="722f0-105">In this section</span></span>



| <span data-ttu-id="722f0-106">Tema</span><span class="sxs-lookup"><span data-stu-id="722f0-106">Topic</span></span>                                                                   | <span data-ttu-id="722f0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="722f0-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="722f0-108">Nomenclatura de archivos, rutas de acceso y espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="722f0-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="722f0-109">Reglas, convenciones y limitaciones de los nombres de archivos y directorios, incluidas las convenciones de nomenclatura, los nombres de archivo cortos y los nombres de archivo largos, rutas de acceso completas frente a rutas de acceso relativas, límite de longitud de ruta de acceso máxima, nombres de archivo de 8,3 y espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="722f0-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="722f0-110">Crear y abrir archivos</span><span class="sxs-lookup"><span data-stu-id="722f0-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="722f0-111">Consideraciones para crear o abrir un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="722f0-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="722f0-112">Mover y reemplazar archivos</span><span class="sxs-lookup"><span data-stu-id="722f0-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="722f0-113">Consideraciones para mover y reemplazar archivos mediante las funciones CopyFileEx, CreateFile, Replacefile y MoveFileEx.</span><span class="sxs-lookup"><span data-stu-id="722f0-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="722f0-114">Cerrar y eliminar archivos</span><span class="sxs-lookup"><span data-stu-id="722f0-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="722f0-115">Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="722f0-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="722f0-116">Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="722f0-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="722f0-117">Desfragmentar archivos</span><span class="sxs-lookup"><span data-stu-id="722f0-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="722f0-118">La *desfragmentación* es el proceso por el que se mueven partes de los archivos en un disco para desfragmentar archivos, es decir, el proceso de mover los clústeres de archivos de un disco para que sean contiguos.</span><span class="sxs-lookup"><span data-stu-id="722f0-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

