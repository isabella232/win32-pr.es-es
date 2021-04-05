---
description: La API de Direct3D define varios elementos de API que le ayudarán a crear y administrar el sistema de efectos.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Referencia de efectos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000564"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="7bb49-103">Referencia de efectos (gráficos de Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7bb49-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="7bb49-104">La API de Direct3D define varios elementos de API que le ayudarán a crear y administrar el sistema de efectos.</span><span class="sxs-lookup"><span data-stu-id="7bb49-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="7bb49-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7bb49-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="7bb49-106">Funciones</span><span class="sxs-lookup"><span data-stu-id="7bb49-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="7bb49-107">Estructuras</span><span class="sxs-lookup"><span data-stu-id="7bb49-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="7bb49-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="7bb49-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="7bb49-109">El sistema de efectos encapsula las asignaciones de estado en un efecto.</span><span class="sxs-lookup"><span data-stu-id="7bb49-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="7bb49-110">Cada efecto es una colección de estado de la canalización que se puede dividir en las asignaciones de estado mediante bloques de estado, recursos y sombreadores.</span><span class="sxs-lookup"><span data-stu-id="7bb49-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="7bb49-111">Dependiendo del tamaño de un efecto, puede optar por implementar uno en una cadena de texto ASCII o en un archivo de efectos (. FX).</span><span class="sxs-lookup"><span data-stu-id="7bb49-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="7bb49-112">Para organizar la información de un efecto, vea el [formato del efecto](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="7bb49-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="7bb49-113">Una vez que haya diseñado un efecto, use la API de efecto para establecer el estado en el dispositivo durante la representación.</span><span class="sxs-lookup"><span data-stu-id="7bb49-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="7bb49-114">Además, el sistema de efectos es compatible con una serie de API de reflexión para obtener y establecer datos de efectos.</span><span class="sxs-lookup"><span data-stu-id="7bb49-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="7bb49-115">Para obtener más información, vea [interfaces del sistema de efectos (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7bb49-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bb49-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bb49-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bb49-117">Referencia de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7bb49-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



