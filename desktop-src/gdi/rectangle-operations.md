---
description: La función SetRect crea un rectángulo, la función CopyRect realiza una copia de un rectángulo determinado y la función SetRectEmpty crea un rectángulo vacío.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operaciones de rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360527"
---
# <a name="rectangle-operations"></a><span data-ttu-id="75df8-103">Operaciones de rectángulo</span><span class="sxs-lookup"><span data-stu-id="75df8-103">Rectangle Operations</span></span>

<span data-ttu-id="75df8-104">La función [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rectángulo, la función [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) realiza una copia de un rectángulo determinado y la función [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rectángulo vacío.</span><span class="sxs-lookup"><span data-stu-id="75df8-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="75df8-105">Un rectángulo vacío es cualquier rectángulo que tenga un ancho de cero, un alto de cero o ambos.</span><span class="sxs-lookup"><span data-stu-id="75df8-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="75df8-106">La función [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina si un rectángulo determinado está vacío.</span><span class="sxs-lookup"><span data-stu-id="75df8-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="75df8-107">La función [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina si dos rectángulos son idénticos, es decir, si tienen las mismas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="75df8-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="75df8-108">La función [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o disminuye el ancho o el alto de un rectángulo, o ambos.</span><span class="sxs-lookup"><span data-stu-id="75df8-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="75df8-109">Puede Agregar o quitar el ancho de ambos extremos del rectángulo; puede Agregar o quitar el alto de la parte superior e inferior del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="75df8-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="75df8-110">La función [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) mueve un rectángulo en una cantidad determinada.</span><span class="sxs-lookup"><span data-stu-id="75df8-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="75df8-111">Mueve el rectángulo agregando las cifras x-amount, y amount, o x-e y-amount especificadas a las coordenadas de la esquina.</span><span class="sxs-lookup"><span data-stu-id="75df8-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="75df8-112">La función [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina si un punto determinado se encuentra dentro de un rectángulo determinado.</span><span class="sxs-lookup"><span data-stu-id="75df8-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="75df8-113">El punto está en el rectángulo si se encuentra en el lado izquierdo o superior o está completamente dentro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="75df8-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="75df8-114">El punto no está en el rectángulo si se encuentra en el lado derecho o en el inferior.</span><span class="sxs-lookup"><span data-stu-id="75df8-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="75df8-115">La función [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuevo rectángulo que es la intersección de dos rectángulos existentes, tal como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="75df8-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="75df8-116">Ilustración que muestra dos rectángulos superpuestos, con un sombreado más oscuro para indicar la intersección</span><span class="sxs-lookup"><span data-stu-id="75df8-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="75df8-117">La función [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuevo rectángulo que es la Unión de dos rectángulos existentes, tal como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="75df8-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![Ilustración de dos rectángulos superpuestos, con un sombreado más oscuro que indica áreas dentro de la Unión, pero no dentro de un rectángulo](images/csrec-02.png)

<span data-ttu-id="75df8-119">Para obtener información sobre las funciones que dibujan elipses y polígonos, vea [formas rellenas](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="75df8-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



