---
description: En este ejemplo se muestra cómo crear un paquete de revisión que aplica una pequeña actualización al paquete de instalación de ejemplo que se describe en un ejemplo de instalación.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Un pequeño ejemplo de revisión de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667072"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="4bffe-103">Un pequeño ejemplo de revisión de actualización</span><span class="sxs-lookup"><span data-stu-id="4bffe-103">A Small Update Patching Example</span></span>

<span data-ttu-id="4bffe-104">En este ejemplo se muestra cómo crear un [paquete de revisión](patch-packages.md) que aplica una [pequeña actualización](small-updates.md) al paquete de instalación de ejemplo que se describe en [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="4bffe-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="4bffe-105">Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que se consideran demasiado pequeños para garantizar el cambio del código de producto.</span><span class="sxs-lookup"><span data-stu-id="4bffe-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="4bffe-106">Para obtener más información [, consulte revisiones y actualizaciones](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="4bffe-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="4bffe-107">En este ejemplo se muestra cómo crear un paquete de revisión de Windows Installer que actualiza la característica de concierto de la MNP2000 de producto hipotética para corregir un error en el producto original.</span><span class="sxs-lookup"><span data-stu-id="4bffe-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="4bffe-108">El paquete de revisión de ejemplo aplica una pequeña actualización al producto que no requiere cambiar el código de producto.</span><span class="sxs-lookup"><span data-stu-id="4bffe-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="4bffe-109">Consulte el tema sobre las [actualizaciones principales](major-upgrades.md) en la sección [revisiones y actualizaciones](patching-and-upgrades.md) para obtener más información sobre las actualizaciones principales.</span><span class="sxs-lookup"><span data-stu-id="4bffe-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="4bffe-110">El paquete de actualización de ejemplo tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="4bffe-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="4bffe-111">Corrige un error leve en la programación del concierto que muestra la característica de concierto.</span><span class="sxs-lookup"><span data-stu-id="4bffe-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="4bffe-112">Actualiza el código de paquete para reflejar que el paquete de instalación ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4bffe-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="4bffe-113">La actualización pequeña se puede aplicar revisando la instalación local del producto.</span><span class="sxs-lookup"><span data-stu-id="4bffe-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="4bffe-114">Continuar</span><span class="sxs-lookup"><span data-stu-id="4bffe-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



