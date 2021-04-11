---
description: El objeto Merge proporciona acceso a otros objetos de nivel superior. Se debe crear un objeto Merge antes de cargar la compatibilidad de automatización que requiere COM para tener acceso a las funciones de Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Merge (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279149"
---
# <a name="merge-object"></a><span data-ttu-id="c571f-104">Merge (objeto)</span><span class="sxs-lookup"><span data-stu-id="c571f-104">Merge Object</span></span>

<span data-ttu-id="c571f-105">El objeto **Merge** proporciona acceso a otros objetos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c571f-105">The **Merge** object provides access to other top-level objects.</span></span> <span data-ttu-id="c571f-106">Se debe crear un objeto **Merge** antes de cargar la compatibilidad de automatización que requiere com para tener acceso a las funciones de Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="c571f-106">A **Merge** object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.</span></span>

<span data-ttu-id="c571f-107">Mergemod.dll proporciona acceso a la funcionalidad extendida en tiempo de compilación a través de una segunda versión del CLSID existente.</span><span class="sxs-lookup"><span data-stu-id="c571f-107">Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID.</span></span> <span data-ttu-id="c571f-108">Este CLSID admite la funcionalidad existente disponible a través de la interfaz [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , pero la interfaz predeterminada en el objeto (y la interfaz dual asociada) es la interfaz [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) en lugar de la interfaz **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="c571f-108">This CLSID supports existing functionality available through the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) interface, but the default interface on the object (and the associated dual interface) is the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) interface instead of the **IMsmMerge** interface.</span></span>

 

 
