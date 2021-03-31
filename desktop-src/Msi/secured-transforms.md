---
description: Las transformaciones protegidas a veces son necesarias por motivos de seguridad.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformaciones protegidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913658"
---
# <a name="secured-transforms"></a><span data-ttu-id="83350-103">Transformaciones protegidas</span><span class="sxs-lookup"><span data-stu-id="83350-103">Secured Transforms</span></span>

<span data-ttu-id="83350-104">Las transformaciones protegidas a veces son necesarias por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="83350-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="83350-105">Las transformaciones protegidas se almacenan localmente en el equipo del usuario en una ubicación en la que, en un sistema de archivos seguro, el usuario no tiene acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="83350-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="83350-106">Dichas transformaciones se almacenan en caché en esta ubicación durante la instalación o el anuncio del paquete.</span><span class="sxs-lookup"><span data-stu-id="83350-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="83350-107">Solo los administradores y el sistema local tienen acceso de escritura a esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="83350-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="83350-108">Un usuario que no sea administrador no podrá modificar el archivo de transformación.</span><span class="sxs-lookup"><span data-stu-id="83350-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="83350-109">Durante la [instalación](installation-on-demand.md) posterior a petición o las [instalaciones de mantenimiento](maintenance-installation.md) del paquete, el instalador usa las transformaciones almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="83350-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="83350-110">Para especificar el almacenamiento de transformación seguro, establezca la [Directiva TransformsSecure](transformssecure-policy.md), establezca la propiedad [**TransformsSecure**](transformssecure.md) o pase el símbolo @ o \| en la lista transformaciones.</span><span class="sxs-lookup"><span data-stu-id="83350-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="83350-111">Tenga en cuenta que no puede incluir transformaciones seguras y no seguras en la misma lista de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="83350-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="83350-112">Consulte [aplicar transformaciones](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="83350-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="83350-113">La eliminación del producto por cualquier usuario quita todas las transformaciones protegidas de ese producto del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="83350-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="83350-114">Si el instalador detecta que una transformación protegida no está disponible localmente, intenta restaurar la memoria caché de transformación desde un origen.</span><span class="sxs-lookup"><span data-stu-id="83350-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="83350-115">Las transformaciones seguras pueden ser seguras en el origen o en una ruta de acceso completa:</span><span class="sxs-lookup"><span data-stu-id="83350-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="83350-116">Las [transformaciones seguras en el origen](secure-at-source-transforms.md) que faltan en la memoria caché de transformación local se restauran desde la raíz del origen del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="83350-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="83350-117">Las [transformaciones de ruta de acceso completas seguras](secure-full-path-transforms.md) que faltan en la memoria caché de transformación local se restauran desde la ruta de acceso completa original especificada por la lista de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="83350-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



