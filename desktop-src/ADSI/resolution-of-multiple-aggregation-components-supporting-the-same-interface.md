---
title: Resolución de varios componentes de agregación que admiten la misma interfaz
description: No es habitual que dos extensiones expongan la misma interfaz a ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Resolución de varios componentes de agregación que admiten la misma interfaz ADSI
- resolución de varios componentes de agregación que admiten la misma interfaz ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656157"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="74ae2-105">Resolución de varios componentes de agregación que admiten la misma interfaz</span><span class="sxs-lookup"><span data-stu-id="74ae2-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="74ae2-106">No es habitual que dos extensiones expongan la misma interfaz a ADSI.</span><span class="sxs-lookup"><span data-stu-id="74ae2-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="74ae2-107">Si esto ocurre, se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="74ae2-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="74ae2-108">Si una interfaz, como **IMyInterface**, es compatible con el agregador (ADSI) y cualquier objeto de extensión, **QueryInterface** siempre devuelve el **IMyInterface** de ADSI.</span><span class="sxs-lookup"><span data-stu-id="74ae2-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="74ae2-109">Si el agregador (ADSI) no admite una interfaz, como **IMyInterface**, pero es compatible con más de un objeto de extensión, **QueryInterface** devuelve el **IMyInterface** del primer objeto de extensión enumerado en el registro que admite la interfaz.</span><span class="sxs-lookup"><span data-stu-id="74ae2-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="74ae2-110">Tenga en cuenta que el orden de los componentes del registro también afecta a la resolución de conflictos de nombres en la automatización.</span><span class="sxs-lookup"><span data-stu-id="74ae2-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="74ae2-111">Para obtener más información, consulte [resolución de conflictos de nombres de función y propiedad en Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="74ae2-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 




