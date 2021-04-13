---
title: Recorte (OpenGL)
description: El recorte se produce en dos pasos
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Canalización de procesamiento de OpenGL, recorte
- recorte de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421820"
---
# <a name="clipping-opengl"></a><span data-ttu-id="6a2bb-105">Recorte (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="6a2bb-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="6a2bb-106">El recorte se produce en dos pasos:</span><span class="sxs-lookup"><span data-stu-id="6a2bb-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="6a2bb-107">**Ver el recorte específico del clippingApplication de volumen.**</span><span class="sxs-lookup"><span data-stu-id="6a2bb-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="6a2bb-108">Inmediatamente después de ensamblar los primitivos, se recortan en coordenadas oculares según sea necesario para los planos de recorte que haya definido con [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="6a2bb-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="6a2bb-109">(OpenGL requiere compatibilidad con al menos seis planos de recorte específicos de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="6a2bb-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="6a2bb-110">Las primitivas se transforman mediante la matriz de proyección en coordenadas de recorte y se recortan por el volumen de vista correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6a2bb-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="6a2bb-111">Esta matriz se puede controlar mediante las funciones de transformación de matriz (vea [transformaciones de matriz](matrix-transformations.md)) pero normalmente se especifica mediante [**glFrustum**](glfrustum.md) o [**glOrtho**](glortho.md).</span><span class="sxs-lookup"><span data-stu-id="6a2bb-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="6a2bb-112">Los puntos, segmentos de línea y polígonos se controlan de forma diferente durante el recorte:</span><span class="sxs-lookup"><span data-stu-id="6a2bb-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="6a2bb-113">Los puntos se retienen en su estado original (si están dentro del volumen de clip) o se descartan (si están fuera del volumen de clip).</span><span class="sxs-lookup"><span data-stu-id="6a2bb-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="6a2bb-114">Si partes de segmentos de línea o polígonos están fuera del volumen de clip, se generan nuevos vértices en los puntos de recorte.</span><span class="sxs-lookup"><span data-stu-id="6a2bb-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="6a2bb-115">En el caso de los polígonos, es posible que sea necesario construir un borde completo entre los nuevos vértices generados en los puntos de recorte.</span><span class="sxs-lookup"><span data-stu-id="6a2bb-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="6a2bb-116">En el caso de segmentos de línea y polígonos que se recortan, la información de marca de borde, color y textura se asigna a todos los nuevos vértices.</span><span class="sxs-lookup"><span data-stu-id="6a2bb-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




