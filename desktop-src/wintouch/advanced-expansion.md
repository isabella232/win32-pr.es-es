---
title: Expansión avanzada
description: Expansión avanzada
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Touch de Windows, expansión
- Touch de Windows, expansión avanzada
- Windows Touch, manipulaciones
- manipulaciones, expansión
- manipulaciones, expansión avanzada
- expansión, avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268341"
---
# <a name="advanced-expansion"></a><span data-ttu-id="216ef-109">Expansión avanzada</span><span class="sxs-lookup"><span data-stu-id="216ef-109">Advanced Expansion</span></span>

<span data-ttu-id="216ef-110">En la ilustración siguiente se muestran dos formas de expandir un objeto.</span><span class="sxs-lookup"><span data-stu-id="216ef-110">The following illustration shows two ways that an object can be expanded.</span></span>

![Ilustración en la que se muestra la expansión simple en torno al punto central de un objeto y la expansión avanzada en torno al punto central de la manipulación](images/expansion.png)

<span data-ttu-id="216ef-112">En el ejemplo A, el ejemplo de expansión simple, el objeto se expande alrededor de su punto central.</span><span class="sxs-lookup"><span data-stu-id="216ef-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="216ef-113">En el ejemplo B, el objeto se expande alrededor del punto central de la manipulación.</span><span class="sxs-lookup"><span data-stu-id="216ef-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="216ef-114">Para habilitarlo, debe traducir el objeto mientras se expande.</span><span class="sxs-lookup"><span data-stu-id="216ef-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="216ef-115">La cantidad que se va a trasladar el objeto es la misma que la distancia desde el centro del objeto hasta el punto central del gesto.</span><span class="sxs-lookup"><span data-stu-id="216ef-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="216ef-116">De forma intuitiva, es como si se expande el objeto desde el punto central del gesto de expansión y, a continuación, se mueve para que siga en el mismo centro que su posición inicial.</span><span class="sxs-lookup"><span data-stu-id="216ef-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="216ef-117">En el código siguiente se muestra una manera de aplicar este concepto para habilitar la expansión en torno a un punto central.</span><span class="sxs-lookup"><span data-stu-id="216ef-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="216ef-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="216ef-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="216ef-119">Manipulaciones</span><span class="sxs-lookup"><span data-stu-id="216ef-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




