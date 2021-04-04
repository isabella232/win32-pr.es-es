---
title: Interfaces privadas de Visual Basic
description: Interfaces privadas de Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076368"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="963f4-103">Interfaces privadas de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="963f4-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="963f4-104">Dos interfaces que se implementan mediante Visual Basic se identifican aquí para las categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="963f4-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="963f4-105">No se espera que los controles requieran estas categorías porque es posible que los controles ofrezcan funcionalidad alternativa cuando no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="963f4-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="963f4-106">La interfaz [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que los controles se integren mejor en el entorno de Visual Basic al dar formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="963f4-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="963f4-107">CATId-{02496840-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBFormat</span><span class="sxs-lookup"><span data-stu-id="963f4-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="963f4-108">La interfaz [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite a un control enumerar otros controles en el formulario de VB.</span><span class="sxs-lookup"><span data-stu-id="963f4-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="963f4-109">CATId-{02496841-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBGetControl</span><span class="sxs-lookup"><span data-stu-id="963f4-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="963f4-110">Aquí se describen dos interfaces privadas adicionales, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) y [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), aunque no definen categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="963f4-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="963f4-111">No se recomienda el uso de estas cuatro interfaces porque no son compatibles con los contenedores que no son Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="963f4-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="963f4-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="963f4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="963f4-113">Categorías del componente</span><span class="sxs-lookup"><span data-stu-id="963f4-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




