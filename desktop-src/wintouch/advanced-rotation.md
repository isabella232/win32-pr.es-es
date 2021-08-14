---
title: Rotación avanzada
description: En esta sección se explica cómo girar un objeto en función de dónde el usuario realiza la manipulación de rotación.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Táctil, rotación
- Windows Táctil, rotación avanzada
- Windows Touch,manipulations
- manipulaciones, rotación
- manipulaciones, rotación avanzada
- rotation,advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dda17ae8076061f7b5b7b935afb2b7f8e5fb10cb270280f7edbb8c23aa896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199521"
---
# <a name="advanced-rotation"></a>Rotación avanzada

En esta sección se explica cómo girar un objeto en función de dónde el usuario realiza la manipulación de rotación.

En la imagen siguiente se muestran dos maneras diferentes de girar un objeto.

![Ilustración en la que se muestran dos tipos de rotación con un solo dedo: alrededor del centro o alrededor del borde, con el borde que implica la rotación y la traducción](images/rotation.png)

En el ejemplo A, el objeto se manipula alrededor del punto central del objeto. En el ejemplo B, el objeto gira alrededor del punto central de la manipulación. Para admitir la manipulación en torno a un punto distinto del punto central del objeto, debe realizar una manipulación compuesta que realice la rotación y la traducción. El código siguiente muestra cómo se realiza y calcula esta manipulación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones avanzadas](advanced-manipulations.md)
</dt> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




