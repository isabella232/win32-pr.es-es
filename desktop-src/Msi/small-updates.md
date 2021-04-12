---
description: Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que son demasiado pequeños para garantizar el cambio del código de producto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Actualizaciones pequeñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153873"
---
# <a name="small-updates"></a><span data-ttu-id="39cf4-103">Actualizaciones pequeñas</span><span class="sxs-lookup"><span data-stu-id="39cf4-103">Small Updates</span></span>

<span data-ttu-id="39cf4-104">Una actualización pequeña realiza cambios en uno o varios archivos de aplicación que son demasiado pequeños para garantizar el cambio del código de producto.</span><span class="sxs-lookup"><span data-stu-id="39cf4-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="39cf4-105">También se suele hacer referencia a una actualización pequeña como una actualización de ingeniería de corrección rápida (QFE).</span><span class="sxs-lookup"><span data-stu-id="39cf4-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="39cf4-106">Una actualización pequeña no permite la reorganización del árbol de componentes de características.</span><span class="sxs-lookup"><span data-stu-id="39cf4-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="39cf4-107">Una actualización pequeña típica solo cambia uno o dos archivos o una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="39cf4-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="39cf4-108">Dado que una actualización pequeña cambia la información en el archivo. msi, se debe cambiar el código del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="39cf4-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="39cf4-109">El código del paquete se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) de la secuencia de información de [Resumen](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="39cf4-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="39cf4-110">El código de producto nunca cambia con una actualización pequeña, por lo que todos los cambios introducidos por una actualización pequeña deben ser coherentes con las directrices descritas en [cambiar el código de producto](changing-the-product-code.md).</span><span class="sxs-lookup"><span data-stu-id="39cf4-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="39cf4-111">Una actualización requiere una [actualización importante](major-upgrades.md) para cambiar el [**ProductCode**](productcode.md).</span><span class="sxs-lookup"><span data-stu-id="39cf4-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="39cf4-112">Si es necesario diferenciar los productos sin cambiar el código de producto, use una [actualización secundaria](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="39cf4-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="39cf4-113">Para obtener información sobre cómo aplicar un pequeño paquete de revisión de actualización a un paquete de Windows Installer, consulte [crear una revisión de actualización pequeña](creating-a-small-update-patch.md), [aplicar actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)y [aplicar pequeñas actualizaciones mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="39cf4-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



