---
description: Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, etc. Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544483"
---
# <a name="graphic-modes"></a><span data-ttu-id="396ef-104">Modos gráficos</span><span class="sxs-lookup"><span data-stu-id="396ef-104">Graphic Modes</span></span>

<span data-ttu-id="396ef-105">Windows admite cinco modos gráficos que permiten a una aplicación especificar cómo se mezclan los colores, dónde aparece la salida, cómo se escala la salida, etc.</span><span class="sxs-lookup"><span data-stu-id="396ef-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="396ef-106">Estos modos, que se almacenan en un controlador de dominio, se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="396ef-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="396ef-107">Modo gráficos</span><span class="sxs-lookup"><span data-stu-id="396ef-107">Graphics mode</span></span> | <span data-ttu-id="396ef-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="396ef-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="396ef-109">Información previa</span><span class="sxs-lookup"><span data-stu-id="396ef-109">Background</span></span>    | <span data-ttu-id="396ef-110">Define cómo se mezclan los colores de fondo con los colores de pantalla o ventana existentes para las operaciones de texto y de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="396ef-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="396ef-111">Dibujo</span><span class="sxs-lookup"><span data-stu-id="396ef-111">Drawing</span></span>       | <span data-ttu-id="396ef-112">Define cómo se mezclan los colores de primer plano con los colores de pantalla o ventana existentes para las operaciones de lápiz, pincel, mapa de bits y texto.</span><span class="sxs-lookup"><span data-stu-id="396ef-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="396ef-113">Asignación</span><span class="sxs-lookup"><span data-stu-id="396ef-113">Mapping</span></span>       | <span data-ttu-id="396ef-114">Define cómo se asignan los resultados de los gráficos del espacio lógico (o del mundo) en la ventana, la pantalla o el papel de la impresora.</span><span class="sxs-lookup"><span data-stu-id="396ef-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="396ef-115">Relleno de polígono</span><span class="sxs-lookup"><span data-stu-id="396ef-115">Polygon-fill</span></span>  | <span data-ttu-id="396ef-116">Define cómo se usa el patrón de pincel para rellenar el interior de regiones complejas.</span><span class="sxs-lookup"><span data-stu-id="396ef-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="396ef-117">Ajuste</span><span class="sxs-lookup"><span data-stu-id="396ef-117">Stretching</span></span>    | <span data-ttu-id="396ef-118">Define cómo se mezclan los colores de los mapas de bits con los colores de pantalla o ventana existentes cuando el mapa de bits se comprime (o se reduce verticalmente).</span><span class="sxs-lookup"><span data-stu-id="396ef-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="396ef-119">Al igual que con los objetos gráficos, el sistema Inicializa un controlador de dominio con los modos gráficos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="396ef-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="396ef-120">Una aplicación puede recuperar y examinar estos modos predeterminados llamando a las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="396ef-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="396ef-121">Modo gráficos</span><span class="sxs-lookup"><span data-stu-id="396ef-121">Graphics mode</span></span> | <span data-ttu-id="396ef-122">Función</span><span class="sxs-lookup"><span data-stu-id="396ef-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="396ef-123">Información previa</span><span class="sxs-lookup"><span data-stu-id="396ef-123">Background</span></span>    | [<span data-ttu-id="396ef-124">**GetBkMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="396ef-125">Dibujo</span><span class="sxs-lookup"><span data-stu-id="396ef-125">Drawing</span></span>       | [<span data-ttu-id="396ef-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="396ef-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="396ef-127">Asignación</span><span class="sxs-lookup"><span data-stu-id="396ef-127">Mapping</span></span>       | [<span data-ttu-id="396ef-128">**GetMapMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="396ef-129">Relleno de polígono</span><span class="sxs-lookup"><span data-stu-id="396ef-129">Polygon-fill</span></span>  | [<span data-ttu-id="396ef-130">**GetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="396ef-131">Ajuste</span><span class="sxs-lookup"><span data-stu-id="396ef-131">Stretching</span></span>    | [<span data-ttu-id="396ef-132">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="396ef-133">Una aplicación puede cambiar los modos predeterminados mediante una llamada a una de las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="396ef-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="396ef-134">Modo gráficos</span><span class="sxs-lookup"><span data-stu-id="396ef-134">Graphics mode</span></span> | <span data-ttu-id="396ef-135">Función</span><span class="sxs-lookup"><span data-stu-id="396ef-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="396ef-136">Información previa</span><span class="sxs-lookup"><span data-stu-id="396ef-136">Background</span></span>    | [<span data-ttu-id="396ef-137">**SetBkMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="396ef-138">Dibujo</span><span class="sxs-lookup"><span data-stu-id="396ef-138">Drawing</span></span>       | [<span data-ttu-id="396ef-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="396ef-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="396ef-140">Asignación</span><span class="sxs-lookup"><span data-stu-id="396ef-140">Mapping</span></span>       | [<span data-ttu-id="396ef-141">**SetMapMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="396ef-142">Relleno de polígono</span><span class="sxs-lookup"><span data-stu-id="396ef-142">Polygon-fill</span></span>  | [<span data-ttu-id="396ef-143">**SetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="396ef-144">Ajuste</span><span class="sxs-lookup"><span data-stu-id="396ef-144">Stretching</span></span>    | [<span data-ttu-id="396ef-145">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="396ef-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



