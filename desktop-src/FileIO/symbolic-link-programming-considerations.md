---
description: Consideraciones de programación para trabajar con vínculos simbólicos.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Consideraciones de programación (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105689682"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="0d6a1-103">Consideraciones de programación (sistemas de archivos locales)</span><span class="sxs-lookup"><span data-stu-id="0d6a1-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="0d6a1-104">Tenga en cuenta las siguientes consideraciones de programación al trabajar con vínculos simbólicos:</span><span class="sxs-lookup"><span data-stu-id="0d6a1-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="0d6a1-105">Los vínculos simbólicos pueden apuntar a un destino no existente.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="0d6a1-106">Al crear un vínculo simbólico, el sistema operativo no comprueba si existe el destino.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="0d6a1-107">Si una aplicación intenta abrir un destino no existente, se devuelve **el \_ archivo de error \_ no \_ encontrado** .</span><span class="sxs-lookup"><span data-stu-id="0d6a1-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="0d6a1-108">Los vínculos simbólicos son puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="0d6a1-109">Para obtener más información, vea [determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="0d6a1-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="0d6a1-110">Hay un máximo de 63 puntos de análisis (y, por lo tanto, vínculos simbólicos) permitidos en una ruta de acceso determinada.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="0d6a1-111">**Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de análisis en una ruta de acceso dada.</span><span class="sxs-lookup"><span data-stu-id="0d6a1-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d6a1-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d6a1-112">Related topics</span></span>

<dl> <span data-ttu-id="0d6a1-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0d6a1-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="0d6a1-114">Vínculos físicos y uniones</span><span class="sxs-lookup"><span data-stu-id="0d6a1-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



