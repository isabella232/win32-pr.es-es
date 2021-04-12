---
description: 'La posición, velocidad y orientación de los orígenes de sonido y agentes de escucha en el espacio 3D se representan mediante coordenadas Cartesianas, que son valores en tres ejes: el eje x, el eje y y el eje z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordenadas del espacio 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277599"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="233f9-103">Coordenadas del espacio 3D</span><span class="sxs-lookup"><span data-stu-id="233f9-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="233f9-104">La posición, velocidad y orientación de los orígenes de sonido y agentes de escucha en el espacio 3D se representan mediante coordenadas Cartesianas, que son valores en tres ejes: el eje x, el eje y y el eje z.</span><span class="sxs-lookup"><span data-stu-id="233f9-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="233f9-105">Los ejes son relativos a un punto de vista establecido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="233f9-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="233f9-106">Los valores del eje x se incrementan de izquierda a derecha, en el eje y, de abajo a arriba, y en el eje z, de Near a Far.</span><span class="sxs-lookup"><span data-stu-id="233f9-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="233f9-107">La estructura de **\_ Vector X3DAUDIO** contiene valores que describen la posición, la velocidad o la orientación en los tres ejes.</span><span class="sxs-lookup"><span data-stu-id="233f9-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="233f9-108">Convencionalmente, los vectores se expresan como tres valores entre paréntesis y separados por comas, en el orden (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="233f9-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="233f9-109">En la posición, los valores están en unidades universales definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="233f9-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="233f9-110">Para la velocidad, el vector describe la velocidad de movimiento a lo largo de cada eje en unidades universales por segundo.</span><span class="sxs-lookup"><span data-stu-id="233f9-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="233f9-111">En el caso de la orientación, los valores se encuentran en unidades arbitrarias y se relacionan entre sí.</span><span class="sxs-lookup"><span data-stu-id="233f9-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="233f9-112">Por ejemplo, si la vista base del mundo 3D está orientada al norte hacia el horizonte y la orientación del agente de escucha es (-1, 0, 1), el agente de escucha está orientado al noroeste.</span><span class="sxs-lookup"><span data-stu-id="233f9-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="233f9-113">Dado que los valores de un vector no están en unidades absolutas, el vector se podría expresar igualmente como (-5, 0, 5) o (-0,25, 0, 0,25).</span><span class="sxs-lookup"><span data-stu-id="233f9-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="233f9-114">los vectores 3D funcionan de forma muy similar a los vectores 2D, pero con un eje adicional en la dirección de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="233f9-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="233f9-115">Para ver cómo funcionan los vectores en el espacio 2D, puede dibujarlos en una hoja de papel.</span><span class="sxs-lookup"><span data-stu-id="233f9-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="233f9-116">Permita que los valores aumenten de la parte inferior a la parte superior del papel y de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="233f9-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="233f9-117">Una línea dibujada de (0,0) a (1,1) tiene la misma orientación, o dirección, que una dibujada de (0,0) a (5, 5).</span><span class="sxs-lookup"><span data-stu-id="233f9-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="233f9-118">Sin embargo, la segunda línea indica una distancia o velocidad mayor.</span><span class="sxs-lookup"><span data-stu-id="233f9-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="233f9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="233f9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="233f9-120">Conceptos de audio comunes</span><span class="sxs-lookup"><span data-stu-id="233f9-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="233f9-121">Información general de X3DAudio</span><span class="sxs-lookup"><span data-stu-id="233f9-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



