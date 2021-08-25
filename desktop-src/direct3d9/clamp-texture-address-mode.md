---
description: El modo de dirección de textura de fijación, identificado por el miembro D3DTADDRESS CLAMP del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D ajuste las coordenadas de textura al intervalo \_ \[ 0.0, 1.0. \]
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modo de dirección de textura de fijación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751365"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Modo de dirección de textura de fijación (Direct3D 9)

El modo de dirección de textura de fijación, identificado por el miembro D3DTADDRESS CLAMP del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D ajuste las coordenadas de textura al intervalo \_ [](./d3dtextureaddress.md) \[ 0.0, 1.0. \] Es decir, se aplica la textura una vez y, a continuación, se desprestigia el color de los píxeles del borde. Por ejemplo, supongamos que la aplicación crea una primitiva cuadrada y asigna coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) y (3.0,0.0) a los vértices de la primitiva. Al establecer el modo de direccionamiento de textura en D3DTADDRESS CLAMP, la textura \_ se aplica una vez. Los colores de píxel en la parte superior de las columnas y el final de las filas se extienden a la parte superior y derecha de la primitiva, respectivamente.

En la ilustración siguiente se muestra una textura fija.

![ilustración de una textura y una textura fija](images/clamp.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
