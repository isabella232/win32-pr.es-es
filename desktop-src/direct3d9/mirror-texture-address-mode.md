---
description: El modo de dirección de textura reflejada, identificado por el miembro D3DTADDRESS MIRROR del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D refleja la textura en cada límite \_ entero.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modo de dirección de textura de reflejo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ef8731c060e95c470bbf8d34222b9ee66e7f9da2c7a6f03a09c2989986ca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728376"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Modo de dirección de textura de reflejo (Direct3D 9)

El modo de dirección de textura reflejada, identificado por el miembro D3DTADDRESS MIRROR del tipo enumerado \_ [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) hace que Direct3D refleja la textura en cada límite entero. Supongamos, por ejemplo, que la aplicación crea una primitiva cuadrada y especifica las coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) y (3.0,0.0). Al establecer el modo de direccionamiento de textura en D3DTADDRESS MIRROR, la textura se aplica tres veces en las direcciones \_ u y v. Todas las demás filas y columnas a las que se aplica es una imagen reflejada de la fila o columna anterior, como se muestra en la ilustración siguiente.

![ilustración de imágenes reflejadas en una cuadrícula de 3x3](images/mirror.png)

Los efectos de este modo de dirección de textura son similares, pero distintos de los del modo de encapsulado. Para obtener más información, vea Ajustar el modo de dirección [de textura (Direct3D 9).](wrap-texture-address-mode.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
