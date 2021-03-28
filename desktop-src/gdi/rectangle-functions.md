---
description: Las siguientes funciones se usan con rectángulos.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Funciones de rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275982"
---
# <a name="rectangle-functions"></a><span data-ttu-id="283cc-103">Funciones de rectángulo</span><span class="sxs-lookup"><span data-stu-id="283cc-103">Rectangle Functions</span></span>

<span data-ttu-id="283cc-104">Las siguientes funciones se usan con rectángulos.</span><span class="sxs-lookup"><span data-stu-id="283cc-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="283cc-105">Función</span><span class="sxs-lookup"><span data-stu-id="283cc-105">Function</span></span>                               | <span data-ttu-id="283cc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="283cc-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="283cc-107">**CopyRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="283cc-108">Copia las coordenadas de un rectángulo en otro.</span><span class="sxs-lookup"><span data-stu-id="283cc-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="283cc-109">**EqualRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="283cc-110">Determina si los dos rectángulos especificados son iguales comparando las coordenadas de las esquinas superior izquierda e inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="283cc-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="283cc-111">**InflateRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="283cc-112">Aumenta o disminuye el ancho y el alto del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="283cc-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="283cc-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="283cc-114">Calcula la intersección de dos rectángulos de origen y coloca las coordenadas del rectángulo de intersección en el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="283cc-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="283cc-115">**IsRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="283cc-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="283cc-116">Determina si el rectángulo especificado está vacío.</span><span class="sxs-lookup"><span data-stu-id="283cc-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="283cc-117">**OffsetRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="283cc-118">Mueve el rectángulo especificado por los desplazamientos especificados.</span><span class="sxs-lookup"><span data-stu-id="283cc-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="283cc-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="283cc-120">Determina si el punto especificado se encuentra dentro del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="283cc-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="283cc-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="283cc-122">Establece las coordenadas del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="283cc-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="283cc-123">**SetRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="283cc-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="283cc-124">Crea un rectángulo vacío en el que todas las coordenadas se establecen en cero.</span><span class="sxs-lookup"><span data-stu-id="283cc-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="283cc-125">**SubtractRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="283cc-126">Determina las coordenadas de un rectángulo formado restando un rectángulo de otro.</span><span class="sxs-lookup"><span data-stu-id="283cc-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="283cc-127">**UnionRect**</span><span class="sxs-lookup"><span data-stu-id="283cc-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="283cc-128">Crea la Unión de dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="283cc-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



