---
description: Un directorio que contiene uno o varios directorios es el elemento primario del directorio o directorios contenidos y cada directorio contenido es un elemento secundario del directorio principal. La estructura jerárquica de los directorios se conoce como un árbol de directorios.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Acerca de la administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907995"
---
# <a name="about-directory-management"></a><span data-ttu-id="d1a6c-104">Acerca de la administración de directorios</span><span class="sxs-lookup"><span data-stu-id="d1a6c-104">About Directory Management</span></span>

<span data-ttu-id="d1a6c-105">Un directorio que contiene uno o varios directorios es el *elemento primario* del directorio o directorios contenidos y cada directorio contenido es un *elemento secundario* del directorio principal.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="d1a6c-106">La estructura jerárquica de los directorios se conoce como un *árbol de directorios*.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="d1a6c-107">El sistema de archivos NTFS implementa el vínculo lógico entre un directorio y los archivos que contiene como una *tabla de entradas de directorio*.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="d1a6c-108">Cuando se mueve un archivo a un directorio, se crea una entrada en la tabla para el archivo que se ha cambiado y el nombre del archivo se coloca en la entrada.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="d1a6c-109">Cuando se elimina un archivo contenido en un directorio, el nombre y la entrada correspondientes al archivo eliminado también se eliminan de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="d1a6c-110">Puede haber más de una entrada para un único archivo en una tabla de entradas de directorio.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="d1a6c-111">Si se crea una entrada adicional en la tabla para un archivo, se hace referencia a esa entrada como un *vínculo físico* a ese archivo.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="d1a6c-112">No hay ningún límite en el número de vínculos físicos que se pueden crear para un único archivo.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="d1a6c-113">Los directorios también pueden contener uniones y puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1a6c-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d1a6c-114">In this section</span></span>



| <span data-ttu-id="d1a6c-115">Tema</span><span class="sxs-lookup"><span data-stu-id="d1a6c-115">Topic</span></span>                                                                                 | <span data-ttu-id="d1a6c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1a6c-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a6c-117">Crear y eliminar directorios</span><span class="sxs-lookup"><span data-stu-id="d1a6c-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="d1a6c-118">Una aplicación puede crear y eliminar directorios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="d1a6c-119">Identificadores de directorio</span><span class="sxs-lookup"><span data-stu-id="d1a6c-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="d1a6c-120">Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="d1a6c-121">Puntos de análisis</span><span class="sxs-lookup"><span data-stu-id="d1a6c-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="d1a6c-122">Describe los puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="d1a6c-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="d1a6c-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1a6c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a6c-124">Referencia de administración de directorios</span><span class="sxs-lookup"><span data-stu-id="d1a6c-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




