---
description: Para que una aplicación pueda representar de manera realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena.
ms.assetid: ff2037e4-2cf6-4247-b93f-13f0078f3b58
title: Asignación de luz con texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5652446562e4c66390d67e11fa624a4a5659b85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705233"
---
# <a name="light-mapping-with-textures-direct3d-9"></a><span data-ttu-id="dc7c7-103">Asignación de luz con texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc7c7-103">Light Mapping with Textures (Direct3D 9)</span></span>

<span data-ttu-id="dc7c7-104">Para que una aplicación pueda representar de manera realista una escena 3D, debe tener en cuenta el efecto que tienen las fuentes de luz en la apariencia de la escena.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-104">For an application to realistically render a 3D scene, it must take into account the effect that light sources have on the appearance of the scene.</span></span> <span data-ttu-id="dc7c7-105">Aunque las técnicas como el sombreado plano y Gouraud son herramientas valiosas en este sentido, pueden ser insuficientes para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-105">Although techniques such as flat and Gouraud shading are valuable tools in this respect, they can be insufficient for your needs.</span></span> <span data-ttu-id="dc7c7-106">Direct3D admite Multipass y varias combinaciones de texturas.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-106">Direct3D supports multipass and multiple texture blending.</span></span> <span data-ttu-id="dc7c7-107">Estas funcionalidades permiten que la aplicación represente escenas con un aspecto más realista que las escenas representadas únicamente con técnicas de sombreado.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-107">These capabilities enable your application to render scenes with a more realistic appearance than scenes rendered with shading techniques alone.</span></span> <span data-ttu-id="dc7c7-108">Al aplicar una o más asignaciones de luz, la aplicación puede asignar áreas de luz y sombra a sus primitivas.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-108">By applying one or more light maps, your application can map areas of light and shadow onto its primitives.</span></span>

<span data-ttu-id="dc7c7-109">Un mapa ligero es una textura o un grupo de texturas que contiene información sobre la iluminación en una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-109">A light map is a texture or group of textures that contains information about lighting in a 3D scene.</span></span> <span data-ttu-id="dc7c7-110">Puede almacenar la información de iluminación en los valores alfa del mapa de luz, en los valores de color, o en ambos.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-110">You can store the lighting information in the alpha values of the light map, in the color values, or in both.</span></span>

<span data-ttu-id="dc7c7-111">Si implementa una asignación ligera mediante la combinación de texturas de Multipass, la aplicación debe representar el mapa de luz en sus primitivas en el primer paso.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-111">If you implement light mapping using multipass texture blending, your application should render the light map onto its primitives on the first pass.</span></span> <span data-ttu-id="dc7c7-112">Debe usar un segundo paso para representar la textura base.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-112">It should use a second pass to render the base texture.</span></span> <span data-ttu-id="dc7c7-113">La excepción a esto es la asignación de luz especular.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-113">The exception to this is specular light mapping.</span></span> <span data-ttu-id="dc7c7-114">En ese caso, represente primero la textura base; a continuación, agregue el mapa de luz.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-114">In that case, render the base texture first; then add the light map.</span></span>

<span data-ttu-id="dc7c7-115">La combinación de texturas múltiples permite a la aplicación representar el mapa de luz y la textura base en un paso.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-115">Multiple texture blending enables your application to render the light map and the base texture in one pass.</span></span> <span data-ttu-id="dc7c7-116">Si el hardware del usuario proporciona varias combinaciones de texturas, la aplicación debe aprovecharse al realizar una asignación ligera.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-116">If the user's hardware provides for multiple texture blending, your application should take advantage of it when performing light mapping.</span></span> <span data-ttu-id="dc7c7-117">Esto mejora significativamente el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-117">This significantly improves your application's performance.</span></span>

<span data-ttu-id="dc7c7-118">Mediante el uso de mapas ligeros, una aplicación de Direct3D puede lograr una gran variedad de efectos de iluminación cuando representa primitivas.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-118">Using light maps, a Direct3D application can achieve a variety of lighting effects when it renders primitives.</span></span> <span data-ttu-id="dc7c7-119">Puede asignar no solo luz monocroma y de color en una escena, sino que también puede agregar detalles como resaltes especulares e iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-119">It can map not only monochrome and colored lights in a scene, but it can also add details such as specular highlights and diffuse lighting.</span></span>

<span data-ttu-id="dc7c7-120">En los temas siguientes se ofrece información sobre el uso de la combinación de texturas de Direct3D para realizar la asignación de luz.</span><span class="sxs-lookup"><span data-stu-id="dc7c7-120">Information on using Direct3D texture blending to perform light mapping is presented in the following topics.</span></span>

-   [<span data-ttu-id="dc7c7-121">Mapas de luz monocroma (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc7c7-121">Monochrome Light Maps (Direct3D 9)</span></span>](monochrome-light-maps.md)
-   [<span data-ttu-id="dc7c7-122">Mapas de luz de color (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc7c7-122">Color Light Maps (Direct3D 9)</span></span>](color-light-maps.md)
-   [<span data-ttu-id="dc7c7-123">Mapas de luz especular (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc7c7-123">Specular Light Maps (Direct3D 9)</span></span>](specular-light-maps.md)
-   [<span data-ttu-id="dc7c7-124">Mapas de luz difusos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dc7c7-124">Diffuse Light Maps (Direct3D 9)</span></span>](diffuse-light-maps.md)

## <a name="related-topics"></a><span data-ttu-id="dc7c7-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc7c7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc7c7-126">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="dc7c7-126">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 



