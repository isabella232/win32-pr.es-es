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
# <a name="advanced-translation"></a>Traducción avanzada

En la ilustración siguiente se muestran dos interpretaciones de la traducción.

![Ilustración que primero muestra la traducción simple, en la que un objeto se mueve sin giro y, a continuación, muestra la traducción avanzada, que implica el movimiento con rotación](images/translation.png)

En el ejemplo A, el ejemplo de traducción simple, el objeto se mueve sin giro. En el ejemplo B, el objeto se gira durante la traducción, dependiendo de dónde se encuentra el punto de contacto del objeto. Si habilita la rotación de un solo dedo como se describe en [rotación de un solo dedo](single-finger-rotation.md), puede habilitar la traducción compleja. En el diagrama siguiente se muestran los distintos componentes de la rotación de un solo dedo cuando se realiza la traducción.

![Ilustración que muestra los componentes de la rotación de un solo dedo: pivotpointx, pivotpointy y pivotradius](images/translation-complex-components.png)

A medida que se mueve el objeto, se vuelve a calcular el radio y se mueve el punto de pivote.

En el código siguiente se muestra una forma de hacerlo en una implementación de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) que habilita la traducción compleja.


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
> Las transformaciones de objeto se producen antes de que se calculen los puntos de pivote y el radio. De esta manera, el objeto se moverá correctamente si el usuario realiza la expansión en el objeto mientras se mueve.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




