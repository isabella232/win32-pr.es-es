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
# <a name="single-finger-rotation"></a>Rotación Single-Finger

En esta sección se explica cómo girar un objeto utilizando un punto de pivote.

En la imagen siguiente se muestra la rotación de un solo dedo.

![Ilustración que muestra dos tipos de rotación de un solo dedo: alrededor del centro o alrededor del borde](images/sfrotation.png)

En el ejemplo A, el objeto se gira alrededor del punto central del objeto utilizando el gesto de giro. En el ejemplo B, el objeto se gira moviendo un solo dedo alrededor del borde del objeto. El procesador de manipulación habilita esta rotación mediante los valores de punto de pivote y radio dinámico. En la imagen siguiente se muestran los componentes de la rotación de un solo dedo.

![Ilustración que muestra los componentes de la rotación de un solo dedo: pivotpointx, pivotpointy y pivotradius](images/sfrotation-components.png)

Después de establecer los valores de [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)y [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , los mensajes de traducción posteriores incorporarán la rotación. Cuanto mayor sea el radio dinámico, mayor será el cambio en x e y debe ser para girar el objeto. En el código siguiente se muestra cómo se pueden establecer estos valores en el procesador de manipulación.


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



En el ejemplo anterior, la distancia al borde del objeto (escalado al 40 por ciento) se usa como el radio dinámico. Dado que se tiene en cuenta el tamaño del objeto, este cálculo es válido para cada Delta de objeto. A medida que el objeto se escala, el radio dinámico crece. Este valor y los valores centrales x e y del objeto se pasan al procesador de manipulación para girar el objeto alrededor del punto de pivote.

> [!Note]  
> El valor de [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca debe estar entre 0,0 y 1,0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




