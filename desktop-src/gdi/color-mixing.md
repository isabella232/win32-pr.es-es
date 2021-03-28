---
description: La combinación de colores permite a una aplicación crear nuevos colores combinando el color del lápiz o del pincel con los colores de la imagen existente.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Combinación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155660"
---
# <a name="color-mixing"></a><span data-ttu-id="12733-103">Combinación de colores</span><span class="sxs-lookup"><span data-stu-id="12733-103">Color Mixing</span></span>

<span data-ttu-id="12733-104">La combinación de colores permite a una aplicación crear nuevos colores combinando el color del lápiz o del pincel con los colores de la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="12733-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="12733-105">La aplicación puede elegir entre dibujar el color del lápiz o del pincel tal como está (dibujando de forma eficaz sobre cualquier imagen existente) o mezclar el color con los colores ya presentes.</span><span class="sxs-lookup"><span data-stu-id="12733-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="12733-106">El modo de combinación de primer plano, que a veces se denomina operación de trama binaria, determina cómo se mezclan estos colores.</span><span class="sxs-lookup"><span data-stu-id="12733-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="12733-107">Una aplicación puede combinar colores, conservando todos los componentes de ambos colores; enmascarar colores, quitar o moderar componentes que no son comunes; o bien, desenmascarar los colores de forma exclusiva, quitar o moderar los componentes que son comunes.</span><span class="sxs-lookup"><span data-stu-id="12733-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="12733-108">Hay varias variaciones en estas operaciones básicas de mezcla.</span><span class="sxs-lookup"><span data-stu-id="12733-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="12733-109">La combinación de colores está sujeta a la aproximación del color.</span><span class="sxs-lookup"><span data-stu-id="12733-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="12733-110">Si el resultado de la combinación de colores es un color que el dispositivo no puede generar, el sistema aproxima el resultado, con un color que puede generar.</span><span class="sxs-lookup"><span data-stu-id="12733-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="12733-111">Si una aplicación mezcla colores propuestos, se mezclan los colores individuales que se usan para crear el color dipuesto, y los resultados están sujetos a la aproximación del color.</span><span class="sxs-lookup"><span data-stu-id="12733-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="12733-112">Una aplicación establece el modo de combinación de primer plano mediante la función [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) y recupera el modo actual mediante la función [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .</span><span class="sxs-lookup"><span data-stu-id="12733-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="12733-113">Aunque hay un modo de combinación en segundo plano, ese modo no controla la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="12733-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="12733-114">En su lugar, especifica si se usa un color de fondo al dibujar líneas con estilo, pinceles tramados y texto.</span><span class="sxs-lookup"><span data-stu-id="12733-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



