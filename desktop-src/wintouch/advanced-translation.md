---
title: Traducción avanzada
description: Traducción avanzada
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch, traducción
- Windows Touch, traducción avanzada
- Windows Touch, manipulaciones
- manipulaciones, traducción
- manipulaciones, traducción avanzada
- traducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903153"
---
# <a name="advanced-translation"></a><span data-ttu-id="eddfb-109">Traducción avanzada</span><span class="sxs-lookup"><span data-stu-id="eddfb-109">Advanced Translation</span></span>

<span data-ttu-id="eddfb-110">En la ilustración siguiente se muestran dos interpretaciones de la traducción.</span><span class="sxs-lookup"><span data-stu-id="eddfb-110">The following illustration shows two interpretations of translation.</span></span>

![Ilustración que primero muestra la traducción simple, en la que un objeto se mueve sin giro y, a continuación, muestra la traducción avanzada, que implica el movimiento con rotación](images/translation.png)

<span data-ttu-id="eddfb-112">En el ejemplo A, el ejemplo de traducción simple, el objeto se mueve sin giro.</span><span class="sxs-lookup"><span data-stu-id="eddfb-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="eddfb-113">En el ejemplo B, el objeto se gira durante la traducción, dependiendo de dónde se encuentra el punto de contacto del objeto.</span><span class="sxs-lookup"><span data-stu-id="eddfb-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="eddfb-114">Si habilita la rotación de un solo dedo como se describe en [rotación de un solo dedo](single-finger-rotation.md), puede habilitar la traducción compleja.</span><span class="sxs-lookup"><span data-stu-id="eddfb-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="eddfb-115">En el diagrama siguiente se muestran los distintos componentes de la rotación de un solo dedo cuando se realiza la traducción.</span><span class="sxs-lookup"><span data-stu-id="eddfb-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![Ilustración que muestra los componentes de la rotación de un solo dedo: pivotpointx, pivotpointy y pivotradius](images/translation-complex-components.png)

<span data-ttu-id="eddfb-117">A medida que se mueve el objeto, se vuelve a calcular el radio y se mueve el punto de pivote.</span><span class="sxs-lookup"><span data-stu-id="eddfb-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="eddfb-118">En el código siguiente se muestra una forma de hacerlo en una implementación de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) que habilita la traducción compleja.</span><span class="sxs-lookup"><span data-stu-id="eddfb-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="eddfb-119">Las transformaciones de objeto se producen antes de que se calculen los puntos de pivote y el radio.</span><span class="sxs-lookup"><span data-stu-id="eddfb-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="eddfb-120">De esta manera, el objeto se moverá correctamente si el usuario realiza la expansión en el objeto mientras se mueve.</span><span class="sxs-lookup"><span data-stu-id="eddfb-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eddfb-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eddfb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eddfb-122">Manipulaciones</span><span class="sxs-lookup"><span data-stu-id="eddfb-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




