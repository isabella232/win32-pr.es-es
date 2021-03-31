---
title: Rotación Single-Finger
description: En esta sección se explica cómo girar un objeto utilizando un punto de pivote.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Touch, rotación
- Windows Touch, manipulaciones
- Windows Touch, rotación de un solo dedo
- Windows Touch, rotación de punto de pivote
- manipulaciones, rotación
- giro, puntos de pivote
- rotación, un dedo
- gestos, rotación de un solo dedo
- rotación de un solo dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903271"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="cf5d9-112">Rotación Single-Finger</span><span class="sxs-lookup"><span data-stu-id="cf5d9-112">Single-Finger Rotation</span></span>

<span data-ttu-id="cf5d9-113">En esta sección se explica cómo girar un objeto utilizando un punto de pivote.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="cf5d9-114">En la imagen siguiente se muestra la rotación de un solo dedo.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-114">The following image illustrates single-finger rotation.</span></span>

![Ilustración que muestra dos tipos de rotación de un solo dedo: alrededor del centro o alrededor del borde](images/sfrotation.png)

<span data-ttu-id="cf5d9-116">En el ejemplo A, el objeto se gira alrededor del punto central del objeto utilizando el gesto de giro.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="cf5d9-117">En el ejemplo B, el objeto se gira moviendo un solo dedo alrededor del borde del objeto.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="cf5d9-118">El procesador de manipulación habilita esta rotación mediante los valores de punto de pivote y radio dinámico.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="cf5d9-119">En la imagen siguiente se muestran los componentes de la rotación de un solo dedo.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-119">The following image illustrates the components of single-finger rotation.</span></span>

![Ilustración que muestra los componentes de la rotación de un solo dedo: pivotpointx, pivotpointy y pivotradius](images/sfrotation-components.png)

<span data-ttu-id="cf5d9-121">Después de establecer los valores de [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)y [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , los mensajes de traducción posteriores incorporarán la rotación.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="cf5d9-122">Cuanto mayor sea el radio dinámico, mayor será el cambio en x e y debe ser para girar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="cf5d9-123">En el código siguiente se muestra cómo se pueden establecer estos valores en el procesador de manipulación.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="cf5d9-124">En el ejemplo anterior, la distancia al borde del objeto (escalado al 40 por ciento) se usa como el radio dinámico.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="cf5d9-125">Dado que se tiene en cuenta el tamaño del objeto, este cálculo es válido para cada Delta de objeto.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="cf5d9-126">A medida que el objeto se escala, el radio dinámico crece.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="cf5d9-127">Este valor y los valores centrales x e y del objeto se pasan al procesador de manipulación para girar el objeto alrededor del punto de pivote.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="cf5d9-128">El valor de [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca debe estar entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="cf5d9-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cf5d9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf5d9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf5d9-130">Manipulaciones</span><span class="sxs-lookup"><span data-stu-id="cf5d9-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="cf5d9-131">**PivotRadius**</span><span class="sxs-lookup"><span data-stu-id="cf5d9-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="cf5d9-132">**PivotPointX**</span><span class="sxs-lookup"><span data-stu-id="cf5d9-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="cf5d9-133">**PivotPointY**</span><span class="sxs-lookup"><span data-stu-id="cf5d9-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




