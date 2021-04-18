---
title: Datos de entrada
description: La canalización de OpenGL requiere que escriba varios tipos de datos
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Canalización de procesamiento de OpenGL, datos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665629"
---
# <a name="input-data"></a><span data-ttu-id="675d1-104">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="675d1-104">Input Data</span></span>

<span data-ttu-id="675d1-105">La canalización de OpenGL requiere que escriba varios tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="675d1-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="675d1-106">**Vértices**.</span><span class="sxs-lookup"><span data-stu-id="675d1-106">**Vertices**.</span></span> <span data-ttu-id="675d1-107">Los vértices describen la forma del objeto geométrico deseado.</span><span class="sxs-lookup"><span data-stu-id="675d1-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="675d1-108">Para especificar vértices, use las funciones [**\* glVertex**](glvertex-functions.md) junto con [**glBegin**](glbegin.md) y [**glEnd**](glend.md) para crear un punto, línea o polígono.</span><span class="sxs-lookup"><span data-stu-id="675d1-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="675d1-109">También puede usar [**glRect**](glrect-functions.md) para describir un rectángulo completo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="675d1-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="675d1-110">**Marca perimetral**.</span><span class="sxs-lookup"><span data-stu-id="675d1-110">**Edge flag**.</span></span> <span data-ttu-id="675d1-111">De forma predeterminada, todos los bordes de polígonos son bordes del límite.</span><span class="sxs-lookup"><span data-stu-id="675d1-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="675d1-112">Use [**glEdgeFlag \***](gledgeflag-functions.md) para establecer explícitamente la marca perimetral.</span><span class="sxs-lookup"><span data-stu-id="675d1-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="675d1-113">**Posición de la trama actual**.</span><span class="sxs-lookup"><span data-stu-id="675d1-113">**Current raster position**.</span></span> <span data-ttu-id="675d1-114">Especificado con [**glRasterPos \***](glrasterpos-functions.md), la posición de la trama actual se usa para determinar las coordenadas de trama para las operaciones de dibujo de píxeles y de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="675d1-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="675d1-115">**Normal actual**.</span><span class="sxs-lookup"><span data-stu-id="675d1-115">**Current normal**.</span></span> <span data-ttu-id="675d1-116">Un vector normal asociado a un vértice determinado determina cómo se orienta una superficie en ese vértice en un espacio tridimensional; Esto, a su vez, afecta a la cantidad de luz que recibe el vértice en particular.</span><span class="sxs-lookup"><span data-stu-id="675d1-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="675d1-117">Use [**glNormal \***](glnormal-functions.md) para especificar un vector normal.</span><span class="sxs-lookup"><span data-stu-id="675d1-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="675d1-118">**Color actual**.</span><span class="sxs-lookup"><span data-stu-id="675d1-118">**Current color**.</span></span> <span data-ttu-id="675d1-119">El color de un vértice, junto con las condiciones de iluminación, determinan el color final iluminado.</span><span class="sxs-lookup"><span data-stu-id="675d1-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="675d1-120">El color se especifica [**con \* glColor**](glcolor-functions.md) si está en modo RGBA, o con [**glIndex \***](glindex-functions.md) si está en modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="675d1-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="675d1-121">**Coordenadas de textura actuales**.</span><span class="sxs-lookup"><span data-stu-id="675d1-121">**Current texture coordinates**.</span></span> <span data-ttu-id="675d1-122">Especificado con [**glTexCoord \***](gltexcoord-functions.md), las coordenadas de textura determinan la ubicación en un mapa de textura que se va a asociar a un vértice de un objeto.</span><span class="sxs-lookup"><span data-stu-id="675d1-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="675d1-123">Cuando se llama a **glVertex \*** , el vértice resultante hereda la marca de borde actual, las coordenadas normal, de color y de textura.</span><span class="sxs-lookup"><span data-stu-id="675d1-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="675d1-124">Por lo tanto, se debe llamar a **glEdgeFlag \***, **glNormal \***, **glColor \*** y **glTexCoord \*** antes de **glVertex \***, en caso de que afecte al vértice resultante.</span><span class="sxs-lookup"><span data-stu-id="675d1-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 




