---
description: La interfaz de dispositivo gráfico (GDI) de Microsoft Windows permite a las aplicaciones utilizar gráficos y texto con formato tanto en la pantalla de vídeo como en la impresora.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: GDI de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985339"
---
# <a name="windows-gdi"></a><span data-ttu-id="e7591-103">GDI de Windows</span><span class="sxs-lookup"><span data-stu-id="e7591-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="e7591-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="e7591-104">Purpose</span></span>

<span data-ttu-id="e7591-105">La interfaz de dispositivo gráfico (GDI) de Microsoft Windows permite a las aplicaciones utilizar gráficos y texto con formato tanto en la pantalla de vídeo como en la impresora.</span><span class="sxs-lookup"><span data-stu-id="e7591-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="e7591-106">Las aplicaciones basadas en Windows no tienen acceso al hardware gráfico directamente.</span><span class="sxs-lookup"><span data-stu-id="e7591-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="e7591-107">En su lugar, GDI interactúa con los controladores de dispositivo en nombre de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e7591-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e7591-108">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="e7591-108">Where applicable</span></span>

<span data-ttu-id="e7591-109">GDI se puede usar en todas las aplicaciones basadas en Windows.</span><span class="sxs-lookup"><span data-stu-id="e7591-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e7591-110">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="e7591-110">Developer audience</span></span>

<span data-ttu-id="e7591-111">Esta API está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="e7591-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="e7591-112">Es necesario estar familiarizado con la [arquitectura controlada por mensajes](../learnwin32/window-messages.md) de Windows.</span><span class="sxs-lookup"><span data-stu-id="e7591-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e7591-113">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="e7591-113">Run-time requirements</span></span>

<span data-ttu-id="e7591-114">Para obtener información sobre los sistemas operativos necesarios para usar una función determinada, consulte la sección de requisitos de la documentación de la función.</span><span class="sxs-lookup"><span data-stu-id="e7591-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e7591-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e7591-115">In this section</span></span>

-   [<span data-ttu-id="e7591-116">Mapas de bits</span><span class="sxs-lookup"><span data-stu-id="e7591-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="e7591-117">Pinceles</span><span class="sxs-lookup"><span data-stu-id="e7591-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="e7591-118">Recorte</span><span class="sxs-lookup"><span data-stu-id="e7591-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="e7591-119">Colores</span><span class="sxs-lookup"><span data-stu-id="e7591-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="e7591-120">Espacios de coordenadas y transformaciones</span><span class="sxs-lookup"><span data-stu-id="e7591-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="e7591-121">Contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e7591-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="e7591-122">Formas rellenas</span><span class="sxs-lookup"><span data-stu-id="e7591-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="e7591-123">Fuentes y texto</span><span class="sxs-lookup"><span data-stu-id="e7591-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="e7591-124">Líneas y curvas</span><span class="sxs-lookup"><span data-stu-id="e7591-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="e7591-125">Metarchivos</span><span class="sxs-lookup"><span data-stu-id="e7591-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="e7591-126">Varios monitores de pantalla</span><span class="sxs-lookup"><span data-stu-id="e7591-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="e7591-127">Dibujar y dibujar</span><span class="sxs-lookup"><span data-stu-id="e7591-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="e7591-128">Paths</span><span class="sxs-lookup"><span data-stu-id="e7591-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="e7591-129">Lápices</span><span class="sxs-lookup"><span data-stu-id="e7591-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="e7591-130">[Impresión y cola de impresión](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7591-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="e7591-131">Rectángulos</span><span class="sxs-lookup"><span data-stu-id="e7591-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="e7591-132">Regiones</span><span class="sxs-lookup"><span data-stu-id="e7591-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="e7591-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7591-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7591-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="e7591-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="e7591-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="e7591-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="e7591-136">OpenGL</span><span class="sxs-lookup"><span data-stu-id="e7591-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="e7591-137">Adquisición de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="e7591-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
