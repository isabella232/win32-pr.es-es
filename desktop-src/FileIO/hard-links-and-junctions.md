---
description: Describe los vínculos físicos y las uniones.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Vínculos físicos y uniones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688464"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="de29d-103">Vínculos físicos y uniones</span><span class="sxs-lookup"><span data-stu-id="de29d-103">Hard Links and Junctions</span></span>

<span data-ttu-id="de29d-104">En el sistema de archivos NTFS se admiten tres tipos de vínculos de archivo: vínculos físicos, uniones y vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="de29d-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="de29d-105">En este tema se ofrece información general sobre vínculos físicos y uniones.</span><span class="sxs-lookup"><span data-stu-id="de29d-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="de29d-106">Para obtener información acerca de los vínculos simbólicos, consulte [crear vínculos simbólicos](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="de29d-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="de29d-107">Vínculos físicos</span><span class="sxs-lookup"><span data-stu-id="de29d-107">Hard Links</span></span>

<span data-ttu-id="de29d-108">Un *vínculo físico* es la representación del sistema de archivos de un archivo por el que hay más de una ruta de acceso que hace referencia a un único archivo en el mismo volumen.</span><span class="sxs-lookup"><span data-stu-id="de29d-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="de29d-109">Para crear un vínculo físico, utilice la función [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) .</span><span class="sxs-lookup"><span data-stu-id="de29d-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="de29d-110">Cualquier cambio que se realice en ese archivo es visible al instante en las aplicaciones que acceden a él a través de los vínculos físicos que hacen referencia a él.</span><span class="sxs-lookup"><span data-stu-id="de29d-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="de29d-111">Sin embargo, el tamaño de la entrada de directorio y la información de atributos solo se actualizan para el vínculo a través del que se realizó el cambio.</span><span class="sxs-lookup"><span data-stu-id="de29d-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="de29d-112">Tenga en cuenta que los atributos del archivo se reflejan en todos los vínculos físicos a ese archivo y los cambios en los atributos de ese archivo se propagan a todos los vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="de29d-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="de29d-113">Por ejemplo, si restablece el atributo READONLY de un vínculo físico para eliminar ese vínculo físico concreto y hay varios vínculos físicos en el archivo real, deberá restablecer el bit de solo lectura en el archivo de uno de los vínculos físicos restantes para volver a colocar el archivo y todos los vínculos físicos restantes en el estado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de29d-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="de29d-114">Por ejemplo, en un sistema donde C: y D: son unidades locales y Z: es una unidad de red asignada a \\ \\ Fred \\ Share, se permiten las siguientes referencias como un vínculo físico:</span><span class="sxs-lookup"><span data-stu-id="de29d-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="de29d-115">C: \\ dira \\ethel.txt vinculado a c \\ : \\ DIRB DIRC \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="de29d-116">D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ DirX \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="de29d-117">C: \\ DirY \\ Bob. bak vinculado a c: \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="de29d-118">Los siguientes elementos no son:</span><span class="sxs-lookup"><span data-stu-id="de29d-118">The following are not:</span></span>

-   <span data-ttu-id="de29d-119">C: \\ dira vinculado a c: \\ DIRB</span><span class="sxs-lookup"><span data-stu-id="de29d-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="de29d-120">C: \\ dira \\ethel.txt vinculado a D \\ : \\ DIRBlucy.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="de29d-121">C: \\ dira \\ethel.txt vinculado a Z \\ : \\ DIRBlucy.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="de29d-122">Para eliminar un vínculo físico, utilice la función [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) .</span><span class="sxs-lookup"><span data-stu-id="de29d-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="de29d-123">Puede eliminar los vínculos físicos en cualquier orden, independientemente del orden en el que se hayan creado.</span><span class="sxs-lookup"><span data-stu-id="de29d-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="de29d-124">Uniones</span><span class="sxs-lookup"><span data-stu-id="de29d-124">Junctions</span></span>

<span data-ttu-id="de29d-125">Una *Unión* (también llamada *Soft Link*) difiere de un vínculo físico en que los objetos de almacenamiento a los que hace referencia son directorios independientes, y una Unión puede vincular directorios ubicados en diferentes volúmenes locales en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="de29d-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="de29d-126">De lo contrario, las uniones funcionan de manera idéntica a los vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="de29d-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="de29d-127">Las uniones se implementan a través de [puntos de reanálisis](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="de29d-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="de29d-128">Suponiendo las mismas condiciones en la sección de vínculos físicos, se permiten las siguientes referencias como uniones:</span><span class="sxs-lookup"><span data-stu-id="de29d-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="de29d-129">C: \\ dira vinculado a c: \\ DIRB \\ DIRC</span><span class="sxs-lookup"><span data-stu-id="de29d-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="de29d-130">C: \\ Celda DirX vinculada a D: \\ DirY</span><span class="sxs-lookup"><span data-stu-id="de29d-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="de29d-131">Los siguientes elementos no son:</span><span class="sxs-lookup"><span data-stu-id="de29d-131">The following are not:</span></span>

-   <span data-ttu-id="de29d-132">C: \\ dira \\one.txt vinculado a C \\ : \\ DIRBtwo.txt</span><span class="sxs-lookup"><span data-stu-id="de29d-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="de29d-133">C: \\ dir1 vinculado a Z: \\ dir2</span><span class="sxs-lookup"><span data-stu-id="de29d-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="de29d-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de29d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de29d-135">Crear vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="de29d-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



