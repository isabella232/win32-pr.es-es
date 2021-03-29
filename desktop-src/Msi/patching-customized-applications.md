---
description: Al instalar una revisión y una o varias transformaciones de personalización en una aplicación, la revisión suele instalarse primero, seguida de las transformaciones de personalización.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Aplicación de revisiones a aplicaciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360709"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="be06c-103">Aplicación de revisiones a aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="be06c-103">Patching Customized Applications</span></span>

<span data-ttu-id="be06c-104">Al instalar una revisión y una o varias transformaciones de personalización en una aplicación, la revisión suele instalarse primero, seguida de las transformaciones de personalización.</span><span class="sxs-lookup"><span data-stu-id="be06c-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="be06c-105">Por diseño, la revisión no está interrumpida por la instalación posterior de la personalización.</span><span class="sxs-lookup"><span data-stu-id="be06c-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="be06c-106">Sin embargo, la instalación de las transformaciones primero y, a continuación, la revisión, puede interrumpir la personalización.</span><span class="sxs-lookup"><span data-stu-id="be06c-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="be06c-107">Por ejemplo, una interrupción en la personalización podría producirse cuando se usa una revisión para actualizar un producto de la versión 1 a la versión 2 y una transformación de personalización que funciona para la versión 1 no funciona para la versión 2.</span><span class="sxs-lookup"><span data-stu-id="be06c-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="be06c-108">En este caso, la revisión de actualización de la versión no se puede aplicar a un producto personalizado sin desinstalar primero y, a continuación, volver a instalar el producto original.</span><span class="sxs-lookup"><span data-stu-id="be06c-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



