---
title: Traducción avanzada
description: Traducción avanzada
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch,translation
- Windows Touch,advanced translation
- Windows Táctil, manipulaciones
- manipulaciones, traducción
- manipulaciones, traducción avanzada
- traducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4712375c12420e076bb93c1240d18dc8e3c1d58006eb24ced7a62a7485e01c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810355"
---
# <a name="advanced-translation"></a>Traducción avanzada

En la ilustración siguiente se muestran dos interpretaciones de la traducción.

![ilustración que muestra primero la traducción simple, en la que un objeto se mueve sin rotación y, a continuación, muestra la traducción avanzada, que implica el movimiento con rotación](images/translation.png)

En el ejemplo A, el ejemplo de traducción simple, el objeto se mueve sin rotación. En el ejemplo B, el objeto se gira durante la traducción, dependiendo de dónde se encuentra el punto de contacto del objeto. Si habilita la rotación con un solo dedo como se describe en Rotación con un solo [dedo](single-finger-rotation.md), puede habilitar la traducción compleja. En el diagrama siguiente se muestran los distintos componentes de rotación con un solo dedo al realizar la traducción.

![ilustración que muestra los componentes de rotación con un solo dedo: pivotpointx, pivotpointy y pivotradius](images/translation-complex-components.png)

A medida que se mueve el objeto, se vuelve a calcular el radio y se mueve el punto de pivote.

El código siguiente muestra una manera de hacerlo en una implementación de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) que permite la traducción compleja.


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
> Las transformaciones de objetos se producen antes de calcular los puntos de pivote y el radio. De esta manera, el objeto se moverá correctamente si el usuario realiza la expansión en el objeto mientras se mueve.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




