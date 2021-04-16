---
description: Las transformaciones que no se han protegido tal y como se describe en transformaciones protegidas son transformaciones no seguras de forma predeterminada.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformaciones no seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678523"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="5385b-103">Transformaciones no seguras</span><span class="sxs-lookup"><span data-stu-id="5385b-103">Unsecured Transforms</span></span>

<span data-ttu-id="5385b-104">Las transformaciones que no se han protegido tal y como se describe en [transformaciones protegidas](secured-transforms.md) son transformaciones no seguras de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5385b-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="5385b-105">Para aplicar una transformación no segura al instalar un paquete, pase los nombres de archivo de transformación en la propiedad de [**TRANSformaciones**](transforms.md) o en la cadena de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5385b-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="5385b-106">No empiece la cadena con los caracteres @ o \| o establezca la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="5385b-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="5385b-107">Tenga en cuenta que no se pueden combinar transformaciones no seguras y [transformaciones protegidas](secured-transforms.md) en la misma lista de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="5385b-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="5385b-108">Si el paquete se instala o se anuncia en el [contexto de instalación](installation-context.md)por usuario y tiene transformaciones no seguras, el instalador guarda el origen de la transformación en la carpeta datos de la aplicación en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="5385b-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="5385b-109">Esto permite al usuario mantener su personalización de un producto mientras se mueve entre equipos.</span><span class="sxs-lookup"><span data-stu-id="5385b-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="5385b-110">Si el paquete se instala o se anuncia en el [contexto de instalación](installation-context.md)por equipo y usa transformaciones no seguras, el instalador guarda el origen de transformación en la carpeta% WINDIR% \\ Installer.</span><span class="sxs-lookup"><span data-stu-id="5385b-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="5385b-111">Durante una instalación del paquete por primera vez, el instalador busca primero la transformación en el origen proporcionado por la propiedad [**TRANSformation**](transforms.md) o la cadena de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5385b-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="5385b-112">Si el origen no está disponible, el instalador busca la transformación en el origen del paquete situado junto al archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="5385b-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="5385b-113">Durante una [instalación de mantenimiento](maintenance-installation.md), el instalador busca la transformación en la ubicación de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="5385b-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="5385b-114">Si la copia almacenada en caché de la transformación deja de estar disponible, el instalador busca la transformación en el origen del paquete situado junto al archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="5385b-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="5385b-115">Para obtener más información, vea [aplicar transformaciones](applying-transforms.md) y [resistencia de origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="5385b-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



