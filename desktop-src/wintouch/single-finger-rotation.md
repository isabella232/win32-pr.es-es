---
title: Single-Finger rotación
description: En esta sección se explica cómo girar un objeto mediante un punto de pivote.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Táctil, rotación
- Windows Touch,manipulations
- Windows Rotación táctil con un solo dedo
- Windows Rotación táctil y de punto de pivote
- manipulaciones, rotación
- rotation,pivot points
- rotation,single-finger
- gestos, rotación con un solo dedo
- rotación con un solo dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110665"
---
# <a name="single-finger-rotation"></a>Single-Finger rotación

En esta sección se explica cómo girar un objeto mediante un punto de pivote.

En la imagen siguiente se muestra la rotación con un solo dedo.

![ilustración en la que se muestran dos tipos de rotación con un solo dedo: alrededor del centro o alrededor del borde](images/sfrotation.png)

En el ejemplo A, el objeto se gira alrededor del punto central del objeto mediante el gesto de rotación. En el ejemplo B, el objeto se gira moviendo un solo dedo alrededor del borde del objeto. El procesador de manipulación habilita esta rotación mediante valores de punto de pivote y radio de pivote. En la imagen siguiente se muestran los componentes de la rotación con un solo dedo.

![ilustración en la que se muestran los componentes de la rotación con un solo dedo: pivotpointx, pivotpointy y pivotradius](images/sfrotation-components.png)

Después de establecer los valores [**de PivotPointX,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)y [**PivotRadius,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) los mensajes de traducción posteriores incorporarán la rotación. Cuanto mayor sea el radio de pivote, mayor será el cambio en x e y para girar el objeto. El código siguiente muestra cómo se podrían establecer estos valores en el procesador de manipulación.


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



En el ejemplo anterior, la distancia al borde del objeto (escalado al 40 por ciento) se usa como radio de pivote. Dado que se tiene en cuenta el tamaño del objeto, este cálculo es válido para cada diferencia de objeto. A medida que el objeto se escala, aumenta el radio de pivote. Este valor y los valores centrales x e y del objeto se pasan al procesador de manipulación para girar el objeto alrededor del punto de pivote.

> [!Note]  
> El [**valor de PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca debe estar entre 0,0 y 1,0.

 

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

 

 




