---
description: Una aplicación recupera las dimensiones del rectángulo delimitador de una región llamando a la función GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recuperar un rectángulo delimitador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811881"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="ef4bf-103">Recuperar un rectángulo delimitador</span><span class="sxs-lookup"><span data-stu-id="ef4bf-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="ef4bf-104">Una aplicación recupera las dimensiones del rectángulo delimitador de una región llamando a la función [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) .</span><span class="sxs-lookup"><span data-stu-id="ef4bf-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="ef4bf-105">Si la región es rectangular, **GetRgnBox** devuelve las dimensiones de la región.</span><span class="sxs-lookup"><span data-stu-id="ef4bf-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="ef4bf-106">Si la región es elíptica, la función devuelve las dimensiones del rectángulo más pequeño que se puede dibujar alrededor de la elipse.</span><span class="sxs-lookup"><span data-stu-id="ef4bf-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="ef4bf-107">Los lados largos del rectángulo tienen la misma longitud que el eje principal de la elipse y los lados cortos del rectángulo tienen la misma longitud que el eje secundario de la elipse.</span><span class="sxs-lookup"><span data-stu-id="ef4bf-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="ef4bf-108">Si la región es poligonal, **GetRgnBox** devuelve las dimensiones del rectángulo más pequeño que se puede dibujar en torno al polígono completo.</span><span class="sxs-lookup"><span data-stu-id="ef4bf-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 



