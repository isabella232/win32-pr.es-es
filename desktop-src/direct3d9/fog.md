---
description: Agregar niebla a una escena 3D puede mejorar el realismo, proporcionar Ambiance o establecer un ambiente, y los artefactos ocultos a veces se producen cuando la geometría distante entra en la vista.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714677"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="86f67-103">Niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="86f67-104">Agregar niebla a una escena 3D puede mejorar el realismo, proporcionar Ambiance o establecer un ambiente, y los artefactos ocultos a veces se producen cuando la geometría distante entra en la vista.</span><span class="sxs-lookup"><span data-stu-id="86f67-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="86f67-105">Direct3D admite dos modelos de niebla, la niebla de píxeles y la niebla de vértice, cada uno con sus propias características e interfaz de programación.</span><span class="sxs-lookup"><span data-stu-id="86f67-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="86f67-106">En esencia, la niebla se implementa mezclando el color de los objetos de una escena con un color de niebla elegido según la profundidad de un objeto en una escena o su distancia desde el punto de vista.</span><span class="sxs-lookup"><span data-stu-id="86f67-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="86f67-107">A medida que los objetos crecen más lejos, su color original se mezcla más y más con el color de niebla elegido, lo que crea la ilusión de que el objeto está siendo cada vez más oculto por partículas diminutas flotantes en la escena.</span><span class="sxs-lookup"><span data-stu-id="86f67-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="86f67-108">En la ilustración siguiente se muestra una escena representada sin niebla y una escena similar representada con niebla habilitada.</span><span class="sxs-lookup"><span data-stu-id="86f67-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![Ilustración de la misma escena con y sin niebla](images/fogcomp.png)

<span data-ttu-id="86f67-110">En esta ilustración, la escena de la izquierda tiene un horizonte claro, más allá del que no hay ningún escenario visible, aunque sería visible en el mundo real.</span><span class="sxs-lookup"><span data-stu-id="86f67-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="86f67-111">La escena de la derecha oculta el horizonte mediante el uso de un color de niebla idéntico al color de fondo, lo que hace que los polígonos parezcan atenuados en la distancia.</span><span class="sxs-lookup"><span data-stu-id="86f67-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="86f67-112">Mediante la combinación de efectos de niebla discretos con el diseño de escenas creativa, puede Agregar el ambiente y suavizar el color de los objetos de una escena.</span><span class="sxs-lookup"><span data-stu-id="86f67-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="86f67-113">Direct3D proporciona dos maneras de agregar niebla a una escena: niebla de píxeles y niebla de vértice, con el nombre de cómo se aplican los efectos de niebla.</span><span class="sxs-lookup"><span data-stu-id="86f67-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="86f67-114">Para obtener más información, consulte [niebla de píxeles (Direct3D 9)](pixel-fog.md) y [niebla de vértice (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="86f67-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="86f67-115">En Resumen, la niebla de píxel (también llamada niebla de tabla) se implementa en el controlador de dispositivo y la niebla de vértices se implementa en el motor de iluminación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="86f67-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="86f67-116">Una aplicación puede implementar la niebla con un sombreador de vértices y la niebla de píxeles simultáneamente si se desea.</span><span class="sxs-lookup"><span data-stu-id="86f67-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="86f67-117">Independientemente de si usa la niebla de píxeles o de vértices, la aplicación debe proporcionar una matriz de proyección compatible para asegurarse de que los efectos de niebla se aplican correctamente.</span><span class="sxs-lookup"><span data-stu-id="86f67-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="86f67-118">Esta restricción se aplica incluso a las aplicaciones que no usan el motor de transformación y luz de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="86f67-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="86f67-119">Para obtener más información sobre cómo puede proporcionar una matriz adecuada, vea [transformación de proyección (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="86f67-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="86f67-120">En los siguientes temas se presenta la niebla y se presenta información sobre el uso de varias características de niebla en aplicaciones de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="86f67-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="86f67-121">Fórmulas de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="86f67-122">Parámetros de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="86f67-123">Combinación de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="86f67-124">Color de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="86f67-125">Niebla de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="86f67-126">Niebla de píxeles (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86f67-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="86f67-127">La combinación de niebla se controla mediante Estados de representación; no forma parte de la canalización de píxeles programable.</span><span class="sxs-lookup"><span data-stu-id="86f67-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86f67-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86f67-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f67-129">Representación en Direct3D</span><span class="sxs-lookup"><span data-stu-id="86f67-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



