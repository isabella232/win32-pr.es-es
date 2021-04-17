---
description: Durante la representación, la canalización interpola los datos de vértices en cada triángulo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolación triangular (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705251"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="7fe69-103">Interpolación triangular (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7fe69-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="7fe69-104">Durante la representación, la canalización interpola los datos de vértices en cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="7fe69-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="7fe69-105">Los datos de vértice pueden ser una amplia variedad de datos y pueden incluir (pero no se limita a): color difuso, color especular, alfa difuso (opacidad del triángulo), alfa especular y un factor de niebla (tomado del alfa especular para la canalización de vértices de función fija y del registro de niebla para la canalización de vértices programable).</span><span class="sxs-lookup"><span data-stu-id="7fe69-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="7fe69-106">Los datos de vértice se definen mediante la [declaración de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="7fe69-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="7fe69-107">En algunos datos de vértices, la interpolación depende del modo de sombreado actual, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7fe69-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="7fe69-108">Modo de sombreado</span><span class="sxs-lookup"><span data-stu-id="7fe69-108">Shading mode</span></span> | <span data-ttu-id="7fe69-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fe69-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe69-110">Plano</span><span class="sxs-lookup"><span data-stu-id="7fe69-110">Flat</span></span>         | <span data-ttu-id="7fe69-111">Solo el factor de niebla se interpola en el modo de sombra plana.</span><span class="sxs-lookup"><span data-stu-id="7fe69-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="7fe69-112">Para todos los demás valores interpolados, el color del primer vértice del triángulo se aplica en toda la esfera.</span><span class="sxs-lookup"><span data-stu-id="7fe69-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="7fe69-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="7fe69-113">Gouraud</span></span>      | <span data-ttu-id="7fe69-114">La interpolación lineal se realiza entre los tres vértices.</span><span class="sxs-lookup"><span data-stu-id="7fe69-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="7fe69-115">El color difuso y el color especular se tratan de forma diferente, dependiendo del modelo de color.</span><span class="sxs-lookup"><span data-stu-id="7fe69-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="7fe69-116">En el modelo de color RGB, el sistema usa los componentes de color rojo, verde y azul en la interpolación.</span><span class="sxs-lookup"><span data-stu-id="7fe69-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="7fe69-117">El componente alfa de un color se trata como un valor interpolado independiente, ya que los controladores de dispositivo pueden implementar la transparencia de dos maneras diferentes: mediante el uso de la combinación de texturas o el uso de punteado.</span><span class="sxs-lookup"><span data-stu-id="7fe69-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="7fe69-118">Use el miembro ShadeCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar qué formas de interpolación admite el controlador de dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="7fe69-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fe69-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe69-120">Sistemas de coordenadas y geometría</span><span class="sxs-lookup"><span data-stu-id="7fe69-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



