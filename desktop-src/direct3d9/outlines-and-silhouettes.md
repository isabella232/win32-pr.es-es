---
description: Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contornos y siluetas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805300"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="dd747-103">Contornos y siluetas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dd747-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="dd747-104">Puede usar el búfer de estarcido para efectos más abstractos, como la esquematización y la silhouetting.</span><span class="sxs-lookup"><span data-stu-id="dd747-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="dd747-105">Si la aplicación aplica una máscara de galería de símbolos a la imagen de un primitivo que tiene la misma forma pero ligeramente más pequeña, la imagen resultante contiene solo el contorno del primitivo.</span><span class="sxs-lookup"><span data-stu-id="dd747-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="dd747-106">A continuación, la aplicación puede rellenar el área enmascarada de estarcido de la imagen con un color sólido, lo que proporciona al primitivo una apariencia en relieve.</span><span class="sxs-lookup"><span data-stu-id="dd747-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="dd747-107">Si la máscara de la galería de símbolos tiene el mismo tamaño y forma que la primitiva que se está representando, la imagen resultante contiene un hueco en el que el primitivo debe ser.</span><span class="sxs-lookup"><span data-stu-id="dd747-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="dd747-108">A continuación, la aplicación puede rellenar el hueco con negro para producir una silueta de la primitiva.</span><span class="sxs-lookup"><span data-stu-id="dd747-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd747-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd747-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd747-110">Técnicas de búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="dd747-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



