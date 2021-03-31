---
description: Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la función CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Crear vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361165"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="bbb63-103">Crear vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="bbb63-103">Creating Symbolic Links</span></span>

<span data-ttu-id="bbb63-104">La función [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) permite crear vínculos simbólicos mediante una ruta de acceso absoluta o relativa.</span><span class="sxs-lookup"><span data-stu-id="bbb63-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="bbb63-105">Los vínculos simbólicos pueden ser vínculos absolutos o relativos.</span><span class="sxs-lookup"><span data-stu-id="bbb63-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="bbb63-106">Los vínculos absolutos son vínculos que especifican cada parte del nombre de ruta de acceso; los vínculos relativos se determinan en relación con los especificadores de vínculo relativo, en una ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="bbb63-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="bbb63-107">Los vínculos relativos se especifican mediante las convenciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="bbb63-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="bbb63-108">Punto (.</span><span class="sxs-lookup"><span data-stu-id="bbb63-108">Dot (.</span></span> <span data-ttu-id="bbb63-109">y..) convenciones, por ejemplo, ".. \\ " resuelve la ruta de acceso relativa al directorio principal.</span><span class="sxs-lookup"><span data-stu-id="bbb63-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="bbb63-110">Los nombres sin barras diagonales ( \) por ejemplo, "tmp" resuelven la ruta de acceso relativa al directorio actual.</span><span class="sxs-lookup"><span data-stu-id="bbb63-110">Names with no slashes (\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="bbb63-111">Relativa a la raíz: por ejemplo, " \\ Windows \\ system32" se resuelve como la "*unidad actual*: \\ Windows \\ system32".</span><span class="sxs-lookup"><span data-stu-id="bbb63-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="bbb63-112">directory</span><span class="sxs-lookup"><span data-stu-id="bbb63-112">directory</span></span>
-   <span data-ttu-id="bbb63-113">Directorio de trabajo actual-relativo: por ejemplo, si el directorio de trabajo actual es "C: \\ Windows \\ system32", "C:File.txt" se resuelve como "c: \\ Windows \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="bbb63-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="bbb63-114">**Nota:**  Si especifica un vínculo relativo al directorio de trabajo actual, se crea como un vínculo absoluto, debido a la manera en que se procesa el directorio de trabajo actual en función del usuario y el subproceso.</span><span class="sxs-lookup"><span data-stu-id="bbb63-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="bbb63-115">Un vínculo simbólico también puede contener tanto puntos de Unión como carpetas montadas como parte del nombre de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bbb63-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="bbb63-116">Los vínculos simbólicos pueden apuntar directamente a un archivo o directorio remoto mediante la ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="bbb63-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="bbb63-117">Los vínculos simbólicos relativos están restringidos a un solo volumen.</span><span class="sxs-lookup"><span data-stu-id="bbb63-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="bbb63-118">Ejemplo de un vínculo simbólico absoluto</span><span class="sxs-lookup"><span data-stu-id="bbb63-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="bbb63-119">En este ejemplo, la ruta de acceso original contiene un componente, '*x*', que es un vínculo simbólico absoluto.</span><span class="sxs-lookup"><span data-stu-id="bbb63-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="bbb63-120">Cuando se encuentra '*x*', el fragmento de la ruta de acceso original hasta e incluye '*x*' se reemplaza completamente por la ruta de acceso a la que apunta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="bbb63-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="bbb63-121">El resto de la ruta de acceso después de "*x*" se anexa a esta nueva ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bbb63-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="bbb63-122">Ahora se convierte en la ruta de acceso modificada.</span><span class="sxs-lookup"><span data-stu-id="bbb63-122">This now becomes the modified path.</span></span>

<span data-ttu-id="bbb63-123">X: "C: \\ alpha \\ beta \\ absLink \\ \\ archivo gamma"</span><span class="sxs-lookup"><span data-stu-id="bbb63-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="bbb63-124">Link: "absLink" se asigna a " \\ \\ machineB \\ share"</span><span class="sxs-lookup"><span data-stu-id="bbb63-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="bbb63-125">Ruta de acceso modificada: " \\ \\ machineB \\ share \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="bbb63-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="bbb63-126">Ejemplo de vínculos simbólicos relativos</span><span class="sxs-lookup"><span data-stu-id="bbb63-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="bbb63-127">En este ejemplo, la ruta de acceso original contiene un componente '*x*', que es un vínculo simbólico relativo.</span><span class="sxs-lookup"><span data-stu-id="bbb63-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="bbb63-128">Cuando se encuentra '*x*', '*x*' se reemplaza completamente por el nuevo fragmento al que apunta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="bbb63-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="bbb63-129">El resto de la ruta de acceso después de '*x*' se anexa a la nueva ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bbb63-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="bbb63-130">Los puntos (..) de esta nueva ruta de acceso reemplazan a los componentes que aparecen delante de los puntos (..).</span><span class="sxs-lookup"><span data-stu-id="bbb63-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="bbb63-131">Cada conjunto de puntos reemplaza al componente anterior.</span><span class="sxs-lookup"><span data-stu-id="bbb63-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="bbb63-132">Si el número de puntos (..) supera el número de componentes, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="bbb63-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="bbb63-133">De lo contrario, cuando haya finalizado todo el reemplazo de componentes, permanecerá la ruta de acceso modificada final.</span><span class="sxs-lookup"><span data-stu-id="bbb63-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="bbb63-134">Archivo gamma X: C: \\ alpha \\ beta \\ Link \\ \\</span><span class="sxs-lookup"><span data-stu-id="bbb63-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="bbb63-135">Link: "link" se asigna a ".. \\ .. \\ Zeta</span><span class="sxs-lookup"><span data-stu-id="bbb63-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="bbb63-136">Ruta de acceso modificada: "C: \\ alpha \\ beta \\ ... \\ . \\ \\archivo gamma Theta \\ "</span><span class="sxs-lookup"><span data-stu-id="bbb63-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="bbb63-137">Ruta final: "C: \\ Theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="bbb63-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbb63-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbb63-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbb63-139">Vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="bbb63-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="bbb63-140">Vínculos físicos y uniones</span><span class="sxs-lookup"><span data-stu-id="bbb63-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="bbb63-141">Nomenclatura de archivos, rutas de acceso y espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="bbb63-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



