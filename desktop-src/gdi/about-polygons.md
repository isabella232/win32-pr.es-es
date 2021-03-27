---
description: Un polígono es una forma rellena con lados rectos.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Acerca de los polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082371"
---
# <a name="about-polygons"></a><span data-ttu-id="b6809-103">Acerca de los polígonos</span><span class="sxs-lookup"><span data-stu-id="b6809-103">About Polygons</span></span>

<span data-ttu-id="b6809-104">Un *polígono* es una forma rellena con lados rectos.</span><span class="sxs-lookup"><span data-stu-id="b6809-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="b6809-105">Los lados de un polígono se dibujan utilizando el lápiz actual.</span><span class="sxs-lookup"><span data-stu-id="b6809-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="b6809-106">Cuando el sistema rellena un polígono, usa el pincel actual y el modo de relleno de polígono actual.</span><span class="sxs-lookup"><span data-stu-id="b6809-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="b6809-107">Los dos modos de relleno, alternativos (el valor predeterminado) y el bobinado, determinan si las regiones dentro de un polígono complejo se rellenan o se dejan sin pintar.</span><span class="sxs-lookup"><span data-stu-id="b6809-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="b6809-108">Una aplicación puede seleccionar cualquier modo llamando a la función [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="b6809-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="b6809-109">Para obtener más información sobre los modos de relleno de polígono, consulte [regiones](regions.md).</span><span class="sxs-lookup"><span data-stu-id="b6809-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="b6809-110">En la ilustración siguiente se muestra un polígono dibujado mediante [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span><span class="sxs-lookup"><span data-stu-id="b6809-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![Ilustración de un polígono en la forma de una estrella de cinco puntas](images/csfsh-04.png)

<span data-ttu-id="b6809-112">Además de dibujar un solo polígono con [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), una aplicación puede dibujar varios polígonos mediante la función de [**polipolígono**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .</span><span class="sxs-lookup"><span data-stu-id="b6809-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
