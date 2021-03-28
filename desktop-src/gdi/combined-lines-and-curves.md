---
description: Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función. Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a la función AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Líneas y curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985027"
---
# <a name="combined-lines-and-curves"></a><span data-ttu-id="6552a-104">Líneas y curvas combinadas</span><span class="sxs-lookup"><span data-stu-id="6552a-104">Combined Lines and Curves</span></span>

<span data-ttu-id="6552a-105">Además de dibujar líneas o curvas, las aplicaciones pueden dibujar combinaciones de salida de línea y curva llamando a una sola función.</span><span class="sxs-lookup"><span data-stu-id="6552a-105">In addition to drawing lines or curves, applications can draw combinations of line and curve output by calling a single function.</span></span> <span data-ttu-id="6552a-106">Por ejemplo, una aplicación puede dibujar el contorno de un gráfico circular mediante una llamada a la función [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .</span><span class="sxs-lookup"><span data-stu-id="6552a-106">For example, an application can draw the outline of a pie chart by calling the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span>

<span data-ttu-id="6552a-107">La función [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) dibuja un arco a lo largo del perímetro de un círculo y dibuja una línea que conecta el punto inicial del arco al centro del círculo.</span><span class="sxs-lookup"><span data-stu-id="6552a-107">The [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function draws an arc along a circle's perimeter and draws a line connecting the starting point of the arc to the circle's center.</span></span> <span data-ttu-id="6552a-108">Además de usar la función **AngleArc** , una aplicación también puede combinar una salida de curva de línea y irregular mediante la función de [**polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .</span><span class="sxs-lookup"><span data-stu-id="6552a-108">In addition to using the **AngleArc** function, an application can also combine line and irregular curve output by using the [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) function.</span></span>

 

 



