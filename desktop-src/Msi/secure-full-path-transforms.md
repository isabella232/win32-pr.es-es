---
description: Las transformaciones de ruta de acceso completa y segura deben tener un origen ubicado en la ruta de acceso completa especificada en la propiedad Transformations.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Transformaciones de ruta de acceso completas seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547094"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="0fdaa-103">Transformaciones de ruta de acceso completas seguras</span><span class="sxs-lookup"><span data-stu-id="0fdaa-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="0fdaa-104">Las transformaciones de ruta de acceso completa y segura deben tener un origen ubicado en la ruta de acceso completa especificada en la propiedad [**TRANSformations**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="0fdaa-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="0fdaa-105">Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en una memoria caché donde, en un sistema de archivos seguro, el usuario no tiene acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="0fdaa-106">Si la copia local de la transformación deja de estar disponible, solo puede restaurar la memoria caché mediante la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="0fdaa-107">La eliminación de un producto por parte de un usuario quita todas las transformaciones seguras para ese producto del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="0fdaa-108">Para aplicar transformaciones de rutas de acceso completas y seguras en la instalación de un paquete, establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) o haga que \| el primer carácter se pase en la lista de transformación.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="0fdaa-109">Las rutas de acceso completas al origen de cada transformación se deben pasar en la cadena de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="0fdaa-110">Si alguna de las rutas de acceso relativas está en la lista, se produce un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="0fdaa-111">No es necesario que el origen de la transformación se encuentre con el origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="0fdaa-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



