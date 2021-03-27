---
description: Las siguientes funciones se usan con líneas y curvas.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Funciones line y Curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997340"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="32c57-103">Funciones line y Curve</span><span class="sxs-lookup"><span data-stu-id="32c57-103">Line and Curve Functions</span></span>

<span data-ttu-id="32c57-104">Las siguientes funciones se usan con líneas y curvas.</span><span class="sxs-lookup"><span data-stu-id="32c57-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="32c57-105">Función</span><span class="sxs-lookup"><span data-stu-id="32c57-105">Function</span></span>                                   | <span data-ttu-id="32c57-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c57-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32c57-107">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="32c57-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="32c57-108">Dibuja un segmento de línea y un arco.</span><span class="sxs-lookup"><span data-stu-id="32c57-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="32c57-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="32c57-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="32c57-110">Dibuja un arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="32c57-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="32c57-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="32c57-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="32c57-112">Dibuja un arco elíptico.</span><span class="sxs-lookup"><span data-stu-id="32c57-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="32c57-113">**GetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="32c57-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="32c57-114">Recupera la dirección de arco actual del contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="32c57-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="32c57-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="32c57-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="32c57-116">Determina qué píxeles deben resaltarse para una línea definida por los puntos inicial y final especificados.</span><span class="sxs-lookup"><span data-stu-id="32c57-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="32c57-117">**LineDDAProc**</span><span class="sxs-lookup"><span data-stu-id="32c57-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="32c57-118">Función de devolución de llamada definida por la aplicación que se usa con la función LineDDA.</span><span class="sxs-lookup"><span data-stu-id="32c57-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="32c57-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="32c57-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="32c57-120">Dibuja una línea desde la posición actual hasta el punto especificado, pero sin incluirlo.</span><span class="sxs-lookup"><span data-stu-id="32c57-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="32c57-121">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="32c57-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="32c57-122">Actualiza la posición actual al punto especificado y, opcionalmente, devuelve la posición anterior.</span><span class="sxs-lookup"><span data-stu-id="32c57-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="32c57-123">**Polibézier**</span><span class="sxs-lookup"><span data-stu-id="32c57-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="32c57-124">Dibuja una o varias curvas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="32c57-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="32c57-125">**Polibézierto**</span><span class="sxs-lookup"><span data-stu-id="32c57-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="32c57-126">Dibuja una o varias curvas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="32c57-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="32c57-127">**Polidraw**</span><span class="sxs-lookup"><span data-stu-id="32c57-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="32c57-128">Dibuja un conjunto de segmentos de línea y curvas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="32c57-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="32c57-129">**Polyline**</span><span class="sxs-lookup"><span data-stu-id="32c57-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="32c57-130">Dibuja una serie de segmentos de línea mediante la conexión de los puntos de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="32c57-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="32c57-131">**Polilineto**</span><span class="sxs-lookup"><span data-stu-id="32c57-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="32c57-132">Dibuja una o varias líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="32c57-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="32c57-133">**Polipolyline**</span><span class="sxs-lookup"><span data-stu-id="32c57-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="32c57-134">Dibuja varias series de segmentos de línea conectados.</span><span class="sxs-lookup"><span data-stu-id="32c57-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="32c57-135">**SetArcDirection**</span><span class="sxs-lookup"><span data-stu-id="32c57-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="32c57-136">Establece la dirección de dibujo que se va a utilizar para las funciones de arco y rectángulo.</span><span class="sxs-lookup"><span data-stu-id="32c57-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



