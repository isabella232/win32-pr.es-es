---
description: Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D. Esta es la idea básica detrás de la técnica de la cartelera.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Cartelera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705385"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="881ee-104">Cartelera (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="881ee-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="881ee-105">Al crear escenas 3D, una aplicación a veces puede obtener ventajas de rendimiento al representar objetos 2D de forma que parezcan objetos 3D.</span><span class="sxs-lookup"><span data-stu-id="881ee-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="881ee-106">Esta es la idea básica detrás de la técnica de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="881ee-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="881ee-107">Una cartelera en el sentido normal de la palabra es un signo a lo largo de un Roadway.</span><span class="sxs-lookup"><span data-stu-id="881ee-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="881ee-108">Las aplicaciones de Microsoft Direct3D pueden crear y representar este tipo de cartelera definiendo un sólido rectangular y aplicándole una textura.</span><span class="sxs-lookup"><span data-stu-id="881ee-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="881ee-109">La cartelera en el sentido más especializado de los gráficos 3D es una extensión de este.</span><span class="sxs-lookup"><span data-stu-id="881ee-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="881ee-110">El objetivo es hacer que los objetos 2D parezcan 3D.</span><span class="sxs-lookup"><span data-stu-id="881ee-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="881ee-111">La técnica consiste en aplicar una textura que contenga la imagen del objeto a un primitivo rectangular.</span><span class="sxs-lookup"><span data-stu-id="881ee-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="881ee-112">La primitiva se gira para que siempre enfrente al usuario.</span><span class="sxs-lookup"><span data-stu-id="881ee-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="881ee-113">No importa si la imagen del objeto no es rectangular.</span><span class="sxs-lookup"><span data-stu-id="881ee-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="881ee-114">Las partes de la cartelera pueden hacerse transparentes, por lo que las partes de la imagen de la cartelera que no desea ver no son visibles.</span><span class="sxs-lookup"><span data-stu-id="881ee-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="881ee-115">Muchos juegos emplean la cartelera de sprites animados.</span><span class="sxs-lookup"><span data-stu-id="881ee-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="881ee-116">Por ejemplo, cuando el usuario está pasando por un laberinto 3D, puede ver armas o recompensas que se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="881ee-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="881ee-117">Suelen ser imágenes 2D con textura en un primitivo rectangular.</span><span class="sxs-lookup"><span data-stu-id="881ee-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="881ee-118">La cartelera se usa a menudo en juegos para representar imágenes de árboles, casquillos y nubes.</span><span class="sxs-lookup"><span data-stu-id="881ee-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="881ee-119">Cuando se aplica una imagen a una cartelera, primero se debe girar el primitivo rectangular para que la imagen resultante se enfrente al usuario.</span><span class="sxs-lookup"><span data-stu-id="881ee-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="881ee-120">A continuación, la aplicación debe convertirla en posición.</span><span class="sxs-lookup"><span data-stu-id="881ee-120">Your application must then translate it into position.</span></span> <span data-ttu-id="881ee-121">A continuación, la aplicación puede aplicar una textura a la primitiva.</span><span class="sxs-lookup"><span data-stu-id="881ee-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="881ee-122">La cartelera funciona mejor para objetos simétricos, especialmente los objetos que son simétricos a lo largo del eje vertical.</span><span class="sxs-lookup"><span data-stu-id="881ee-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="881ee-123">También requiere que la altitud del punto de vista no aumente demasiado.</span><span class="sxs-lookup"><span data-stu-id="881ee-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="881ee-124">Si el usuario tiene permiso para ver la cartelera anterior, se hace evidente de forma fácil que el objeto es 2D en lugar de 3D.</span><span class="sxs-lookup"><span data-stu-id="881ee-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="881ee-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="881ee-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="881ee-126">Ejemplos de alfa</span><span class="sxs-lookup"><span data-stu-id="881ee-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



