---
title: Puntos de portabilidad
description: OpenGL no tiene ningún comando para dibujar un único punto. De lo contrario, las funciones de punto de portabilidad son sencillas. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para los puntos de dibujo y sus funciones de OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Migración de la contabilidad de IRIS, puntos
- trasladar de IRIS GL, puntos
- trasladar a OpenGL desde IRIS GL, puntos
- Exportación de OpenGL desde IRIS GL, puntos
- dibujar funciones, puntos
- puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665690"
---
# <a name="porting-points"></a><span data-ttu-id="f7eed-111">Puntos de portabilidad</span><span class="sxs-lookup"><span data-stu-id="f7eed-111">Porting Points</span></span>

<span data-ttu-id="f7eed-112">OpenGL no tiene ningún comando para dibujar un único punto.</span><span class="sxs-lookup"><span data-stu-id="f7eed-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="f7eed-113">De lo contrario, las funciones de punto de portabilidad son sencillas.</span><span class="sxs-lookup"><span data-stu-id="f7eed-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="f7eed-114">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para los puntos de dibujo y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f7eed-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f7eed-115">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="f7eed-115">IRIS GL function</span></span>           | <span data-ttu-id="f7eed-116">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="f7eed-116">OpenGL function</span></span>                                                   | <span data-ttu-id="f7eed-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f7eed-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eed-118">**PNT**</span><span class="sxs-lookup"><span data-stu-id="f7eed-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="f7eed-119">Dibuja un solo punto.</span><span class="sxs-lookup"><span data-stu-id="f7eed-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="f7eed-120">**bgnpoint**, **extremo**</span><span class="sxs-lookup"><span data-stu-id="f7eed-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="f7eed-121">[**glBegin**](glbegin.md) ( \_ puntos de contabilidad), [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="f7eed-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="f7eed-122">Interpreta los vértices como puntos.</span><span class="sxs-lookup"><span data-stu-id="f7eed-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="f7eed-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="f7eed-123">**pntsize**</span></span>                | [<span data-ttu-id="f7eed-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="f7eed-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="f7eed-125">Establece el tamaño del punto en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f7eed-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="f7eed-126">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="f7eed-126">**pntsmooth**</span></span>              | <span data-ttu-id="f7eed-127">[**glEnable**](glenable.md) (punto de contabilidad \_ \_ suave)</span><span class="sxs-lookup"><span data-stu-id="f7eed-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="f7eed-128">Activa el suavizado de contorno de punto.</span><span class="sxs-lookup"><span data-stu-id="f7eed-128">Turns on point antialiasing.</span></span> <span data-ttu-id="f7eed-129">(Para obtener más información sobre el suavizado de contorno de punto, vea [portar funciones de suavizado de contorno](porting-antialiasing-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="f7eed-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="f7eed-130">Para obtener información sobre las funciones Get relacionadas, vea [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="f7eed-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="f7eed-131">??</span><span class="sxs-lookup"><span data-stu-id="f7eed-131">??</span></span>

 

 




