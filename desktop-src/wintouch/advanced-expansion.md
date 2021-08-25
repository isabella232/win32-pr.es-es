---
title: Expansión avanzada
description: Expansión avanzada
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Touch,expansion
- Windows Táctil, expansión avanzada
- Windows Touch,manipulations
- manipulaciones, expansión
- manipulaciones, expansión avanzada
- expansion,advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e176d91c08bd0d39383e2aba269bbdb5629cfe6b7c2d20eb1ac955786bef2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881505"
---
# <a name="advanced-expansion"></a>Expansión avanzada

En la ilustración siguiente se muestran dos maneras de expandir un objeto.

![ilustración que muestra una expansión simple alrededor del punto central de un objeto y una expansión avanzada alrededor del punto central de la manipulación](images/expansion.png)

En el ejemplo A, el ejemplo de expansión simple, el objeto se expande alrededor de su punto central. En el ejemplo B, el objeto se expande alrededor del punto central de la manipulación. Para habilitarlo, debe traducir el objeto mientras se expande. La cantidad que traducirá el objeto es la misma que la distancia desde el centro del objeto hasta el punto central del gesto. Intuitivamente, es como si fuera a expandir el objeto desde el punto central del gesto de expansión y, a continuación, moverlo para que todavía esté en el mismo centro que su posición inicial. El código siguiente muestra una manera de aplicar este concepto para habilitar la expansión en torno a un punto central.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




