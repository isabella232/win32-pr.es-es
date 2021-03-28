---
description: Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al inicio de la operación de pintura y asigna un píxel en el mapa de bits del pincel al área cliente en el origen de la ventana, que es la esquina superior izquierda de la ventana.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origen del pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565733"
---
# <a name="brush-origin"></a><span data-ttu-id="7250c-103">Origen del pincel</span><span class="sxs-lookup"><span data-stu-id="7250c-103">Brush Origin</span></span>

<span data-ttu-id="7250c-104">Cuando una aplicación llama a una función de dibujo para pintar una forma, el sistema coloca un pincel al inicio de la operación de pintura y asigna un píxel en el mapa de bits del pincel al área cliente en el origen de la *ventana*, que es la esquina superior izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7250c-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="7250c-105">Las coordenadas del píxel que asigna el sistema se denominan *origen del pincel*.</span><span class="sxs-lookup"><span data-stu-id="7250c-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="7250c-106">El origen del pincel predeterminado se encuentra en la esquina superior izquierda del mapa de bits del pincel, en las coordenadas (0,0).</span><span class="sxs-lookup"><span data-stu-id="7250c-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="7250c-107">Después, el sistema copia el pincel en el área cliente, formando un patrón que es tan alto como el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="7250c-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="7250c-108">La operación de copia continúa, fila por fila, hasta que se rellena todo el área cliente.</span><span class="sxs-lookup"><span data-stu-id="7250c-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="7250c-109">Sin embargo, el patrón Brush solo es visible dentro de los límites de la forma especificada.</span><span class="sxs-lookup"><span data-stu-id="7250c-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="7250c-110">Hay instancias cuando no se debe utilizar el origen del pincel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7250c-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="7250c-111">Por ejemplo, puede ser necesario que una aplicación use el mismo pincel para pintar los fondos de sus ventanas principales y secundarias y mezclar el fondo de una ventana secundaria con el de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="7250c-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="7250c-112">Para ello, la aplicación debe restablecer el origen del pincel llamando a la función [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) y desplazando el origen el número necesario de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7250c-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="7250c-113">(Una aplicación puede recuperar el origen del pincel actual llamando a la función [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) ).</span><span class="sxs-lookup"><span data-stu-id="7250c-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="7250c-114">En la ilustración siguiente se muestra una estrella de cinco puntas rellenada con un pincel definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7250c-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="7250c-115">En la ilustración se muestra una imagen ampliada del pincel, así como la ubicación a la que se asignó al principio de la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="7250c-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![Ilustración en la que se muestra que el origen del pincel está asignado al origen de la ventana](images/csbru-01.png)

 

 



