---
title: Usar funciones de suavizado de contorno
description: En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- Migración de la contabilidad de IRIS y suavizado de contorno
- portabilidad de IRIS GL, antialiasing
- trasladar a OpenGL desde IRIS GL, suavizado de contorno
- Exportación de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268578"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="033a9-108">Usar funciones de suavizado de contorno</span><span class="sxs-lookup"><span data-stu-id="033a9-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="033a9-109">En la tabla siguiente se enumeran las funciones de suavizado de contorno de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="033a9-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="033a9-110">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="033a9-110">IRIS GL function</span></span> | <span data-ttu-id="033a9-111">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="033a9-111">OpenGL function</span></span>                                      | <span data-ttu-id="033a9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="033a9-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="033a9-113">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="033a9-113">**pntsmooth**</span></span>    | <span data-ttu-id="033a9-114">[**glEnable**](glenable.md) (punto de contabilidad \_ \_ suave)</span><span class="sxs-lookup"><span data-stu-id="033a9-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="033a9-115">Habilita el suavizado de contorno de los puntos.</span><span class="sxs-lookup"><span data-stu-id="033a9-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="033a9-116">**linesmooth**</span><span class="sxs-lookup"><span data-stu-id="033a9-116">**linesmooth**</span></span>   | <span data-ttu-id="033a9-117">**glEnable**(línea de contabilidad \_ \_ suave)</span><span class="sxs-lookup"><span data-stu-id="033a9-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="033a9-118">Habilita el suavizado de contorno de las líneas.</span><span class="sxs-lookup"><span data-stu-id="033a9-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="033a9-119">**polismooth**</span><span class="sxs-lookup"><span data-stu-id="033a9-119">**polysmooth**</span></span>   | <span data-ttu-id="033a9-120">[**glEnable**](glenable.md) (GL \_ polígono \_ Smooth)</span><span class="sxs-lookup"><span data-stu-id="033a9-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="033a9-121">Habilita el suavizado de contorno de polígonos.</span><span class="sxs-lookup"><span data-stu-id="033a9-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="033a9-122">Use las llamadas [**glDisable**](gldisable.md) equivalentes para desactivar el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="033a9-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="033a9-123">En IRIS GL, puede controlar la calidad del suavizado de contorno llamando a:</span><span class="sxs-lookup"><span data-stu-id="033a9-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="033a9-124">OpenGL proporciona controluse [**glHint**](glhint.md)similares:</span><span class="sxs-lookup"><span data-stu-id="033a9-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="033a9-125">donde *hintMode* es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="033a9-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="033a9-126">Libro \_ de contabilidad más agradable (use el suavizado de mayor calidad).</span><span class="sxs-lookup"><span data-stu-id="033a9-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="033a9-127">GL más \_ rápido (use el suavizado más eficaz).</span><span class="sxs-lookup"><span data-stu-id="033a9-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="033a9-128">no importa el libro de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="033a9-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="033a9-129">IRIS GL también permite la corrección final mediante una llamada a:</span><span class="sxs-lookup"><span data-stu-id="033a9-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="033a9-130">OpenGL no tiene ningún equivalente para esta función.</span><span class="sxs-lookup"><span data-stu-id="033a9-130">OpenGL has no equivalent for this function.</span></span>

 

 




