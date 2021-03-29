---
title: Elección entre el modo RGBA y el Color-Index
description: En general, use el modo RGBA para las aplicaciones de OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como el sombreado, la iluminación, la asignación de colores, la niebla, el suavizado de contorno y la fusión.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL en Windows, modo RGBA
- OpenGL en Windows, modo de índice de color
- Modo RGBA de OpenGL
- modo de índice de color OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775960"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="66bab-107">Elección entre el modo RGBA y el Color-Index</span><span class="sxs-lookup"><span data-stu-id="66bab-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="66bab-108">En general, use el modo RGBA para las aplicaciones de OpenGL; proporciona más flexibilidad que el modo de índice de color para efectos como el sombreado, la iluminación, la asignación de colores, la niebla, el suavizado de contorno y la fusión.</span><span class="sxs-lookup"><span data-stu-id="66bab-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="66bab-109">Considere la posibilidad de usar el modo de índice de color en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="66bab-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="66bab-110">Si tiene un número limitado de bitplanes disponibles; el modo de índice de color puede producir un sombreado menos grueso que el modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="66bab-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="66bab-111">Si no le preocupa el uso de colores "reales"; por ejemplo, el uso de varios colores en un mapa topográfico para designar elevaciones relativas.</span><span class="sxs-lookup"><span data-stu-id="66bab-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="66bab-112">Al migrar una aplicación existente que utiliza el modo de índice de color en gran medida.</span><span class="sxs-lookup"><span data-stu-id="66bab-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="66bab-113">Cuando desee usar la animación y los efectos de mapa de colores en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66bab-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="66bab-114">(Esto no es posible en dispositivos de color verdadero).</span><span class="sxs-lookup"><span data-stu-id="66bab-114">(This is not possible on true-color devices.)</span></span>

 

 




