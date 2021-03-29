---
title: Rotación avanzada
description: En esta sección se explica cómo rotar un objeto en función del lugar en el que el usuario realiza la manipulación de rotación.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Touch, rotación
- Windows Touch, giro avanzado
- Windows Touch, manipulaciones
- manipulaciones, rotación
- manipulaciones, rotación avanzada
- giro, avanzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993945"
---
# <a name="advanced-rotation"></a><span data-ttu-id="e7983-109">Rotación avanzada</span><span class="sxs-lookup"><span data-stu-id="e7983-109">Advanced Rotation</span></span>

<span data-ttu-id="e7983-110">En esta sección se explica cómo rotar un objeto en función del lugar en el que el usuario realiza la manipulación de rotación.</span><span class="sxs-lookup"><span data-stu-id="e7983-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="e7983-111">En la imagen siguiente se muestran dos maneras diferentes de girar un objeto.</span><span class="sxs-lookup"><span data-stu-id="e7983-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![Ilustración que muestra dos tipos de rotación de un solo dedo: alrededor del centro o alrededor del borde, con el borde que implica giro y traslación](images/rotation.png)

<span data-ttu-id="e7983-113">En el ejemplo A, el objeto se manipula alrededor del punto central del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7983-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="e7983-114">En el ejemplo B, el objeto se gira alrededor del punto central de la manipulación.</span><span class="sxs-lookup"><span data-stu-id="e7983-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="e7983-115">Para admitir la manipulación en torno a un punto que no sea el punto central del objeto, debe realizar una manipulación compuesta que realice la rotación y la traslación.</span><span class="sxs-lookup"><span data-stu-id="e7983-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="e7983-116">En el código siguiente se muestra cómo realizar y calcular esta manipulación.</span><span class="sxs-lookup"><span data-stu-id="e7983-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="e7983-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7983-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7983-118">Manipulaciones avanzadas</span><span class="sxs-lookup"><span data-stu-id="e7983-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="e7983-119">Manipulaciones</span><span class="sxs-lookup"><span data-stu-id="e7983-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




