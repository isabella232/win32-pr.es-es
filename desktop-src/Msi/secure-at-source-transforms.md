---
description: Las transformaciones seguras en el origen deben tener un origen ubicado en la raíz del origen del paquete.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformaciones seguras en el origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913661"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="78da5-103">Transformaciones seguras en el origen</span><span class="sxs-lookup"><span data-stu-id="78da5-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="78da5-104">Las transformaciones seguras en el origen deben tener un origen ubicado en la raíz del origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="78da5-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="78da5-105">Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en una memoria caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="78da5-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="78da5-106">Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="78da5-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="78da5-107">El método es el mismo que para buscar un archivo. msi en la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="78da5-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="78da5-108">Para obtener más información, consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="78da5-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="78da5-109">La eliminación de un producto por parte de un usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="78da5-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="78da5-110">Para aplicar transformaciones seguras en el origen a la instalación de un paquete, establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) , o bien haga que @ sea el primer carácter pasado en la lista de transformación.</span><span class="sxs-lookup"><span data-stu-id="78da5-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="78da5-111">Cada transformación se debe indicar mediante un nombre de archivo y debe estar ubicada en la raíz del origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="78da5-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="78da5-112">Si alguna de las transformaciones no se encuentra en la raíz del origen del paquete, se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="78da5-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="78da5-113">Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="78da5-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



