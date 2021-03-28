---
description: Un rectángulo es un polígono de cuatro lados cuyos lados opuestos son paralelos y tienen la misma longitud.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Dibujar rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908491"
---
# <a name="drawing-rectangles"></a><span data-ttu-id="b061b-103">Dibujar rectángulos</span><span class="sxs-lookup"><span data-stu-id="b061b-103">Drawing Rectangles</span></span>

<span data-ttu-id="b061b-104">Un rectángulo es un polígono de cuatro lados cuyos lados opuestos son paralelos y tienen la misma longitud.</span><span class="sxs-lookup"><span data-stu-id="b061b-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="b061b-105">Aunque una aplicación puede dibujar un rectángulo mediante una llamada a la función [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , proporcionando las coordenadas de cada esquina, la función de [**rectángulo**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) proporciona un método más sencillo.</span><span class="sxs-lookup"><span data-stu-id="b061b-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="b061b-106">Esta función solo requiere las coordenadas de la esquina superior izquierda y la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="b061b-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="b061b-107">Cuando una aplicación llama a la función de [**rectángulo**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , el sistema dibuja el rectángulo, excluyendo los lados derecho e inferior si no se establece ninguna transformación universal para el contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b061b-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="b061b-108">Si se ha establecido una transformación universal mediante la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , el sistema incluye los bordes derecho e inferior.</span><span class="sxs-lookup"><span data-stu-id="b061b-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="b061b-109">Además de dibujar un rectángulo tradicional, puede dibujar rectángulos con esquinas redondeadas.</span><span class="sxs-lookup"><span data-stu-id="b061b-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="b061b-110">La función [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) requiere que la aplicación proporcione las coordenadas de las esquinas inferior izquierda y superior derecha, así como el ancho y el alto de la elipse que se usa para redondear cada esquina.</span><span class="sxs-lookup"><span data-stu-id="b061b-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="b061b-111">Las aplicaciones pueden utilizar las siguientes funciones para manipular los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="b061b-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="b061b-112">Función</span><span class="sxs-lookup"><span data-stu-id="b061b-112">Function</span></span>                         | <span data-ttu-id="b061b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b061b-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="b061b-114">**FillRect**</span><span class="sxs-lookup"><span data-stu-id="b061b-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="b061b-115">Vuelve a dibujar el interior de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b061b-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="b061b-116">**FrameRect**</span><span class="sxs-lookup"><span data-stu-id="b061b-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="b061b-117">Vuelve a dibujar los lados de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b061b-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="b061b-118">**InvertRect**</span><span class="sxs-lookup"><span data-stu-id="b061b-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="b061b-119">Invierte los colores que aparecen dentro del interior de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b061b-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 
