---
description: Una aplicación puede dibujar el contorno de una ruta de acceso mediante una llamada a la función StrokePath, que puede rellenar el interior de una ruta de acceso mediante una llamada a la función FillPath, y puede describir y rellenar la ruta de acceso mediante una llamada a la función StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Trazados contornos y rellenos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001520"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="5b2ab-103">Trazados contornos y rellenos</span><span class="sxs-lookup"><span data-stu-id="5b2ab-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="5b2ab-104">Una aplicación puede dibujar el contorno de una ruta de acceso mediante una llamada a la función [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , que puede rellenar el interior de una ruta de acceso mediante una llamada a la función [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) , y puede describir y rellenar la ruta de acceso mediante una llamada a la función [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .</span><span class="sxs-lookup"><span data-stu-id="5b2ab-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="5b2ab-105">Cada vez que una aplicación rellena una ruta de acceso, el sistema utiliza el modo de relleno actual del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="5b2ab-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="5b2ab-106">Una aplicación puede recuperar este modo mediante una llamada a la función [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) , y puede establecer un nuevo modo de relleno mediante una llamada a la función [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="5b2ab-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="5b2ab-107">Para obtener una descripción de los dos modos de relleno, consulte [regiones](regions.md).</span><span class="sxs-lookup"><span data-stu-id="5b2ab-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="5b2ab-108">En la ilustración siguiente se muestra la sección transversal de un objeto creado por una aplicación de diseño asistido por PC (CAD) mediante rutas de acceso que se han esquematizado y rellenado.</span><span class="sxs-lookup"><span data-stu-id="5b2ab-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![Ilustración que muestra la vista transversal de un objeto, con varias partes indicadas por diferentes patrones de relleno](images/cspth-01.png)

 

 



