---
description: 'Hay dos maneras de agregar niebla a una escena: con niebla de píxeles o niebla de vértice.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Tipos de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152118"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="f4642-103">Tipos de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f4642-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="f4642-104">Hay dos maneras de agregar niebla a una escena: con niebla de píxeles o niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="f4642-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="f4642-105">En los temas siguientes se muestran las fórmulas que se usan en las ecuaciones de niebla, así como la implementación de la niebla de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="f4642-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="f4642-106">Una aplicación puede implementar la niebla con un sombreador de vértices y la niebla de píxeles simultáneamente si se desea.</span><span class="sxs-lookup"><span data-stu-id="f4642-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="f4642-107">Fórmulas de niebla</span><span class="sxs-lookup"><span data-stu-id="f4642-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="f4642-108">Parámetros de niebla</span><span class="sxs-lookup"><span data-stu-id="f4642-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="f4642-109">Fusión de niebla</span><span class="sxs-lookup"><span data-stu-id="f4642-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="f4642-110">Color de niebla</span><span class="sxs-lookup"><span data-stu-id="f4642-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="f4642-111">Niebla de vértices</span><span class="sxs-lookup"><span data-stu-id="f4642-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="f4642-112">Niebla de píxeles</span><span class="sxs-lookup"><span data-stu-id="f4642-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="f4642-113">La combinación de niebla se controla mediante Estados de representación; no forma parte de la canalización de píxeles programable.</span><span class="sxs-lookup"><span data-stu-id="f4642-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4642-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4642-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4642-115">Búfer de fotogramas</span><span class="sxs-lookup"><span data-stu-id="f4642-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



