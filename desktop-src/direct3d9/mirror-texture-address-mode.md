---
description: El modo de dirección de textura reflejada, identificado por el \_ miembro reflejado D3DTADDRESS del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D refleje la textura en cada límite de entero.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modo de dirección de textura de reflejo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422856"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Modo de dirección de textura de reflejo (Direct3D 9)

El modo de dirección de textura reflejada, identificado por el \_ miembro reflejado D3DTADDRESS del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D refleje la textura en cada límite de entero. Supongamos, por ejemplo, que la aplicación crea un primitivo cuadrado y especifica las coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0). Al establecer el modo de direccionamiento de textura en el \_ reflejo de D3DTADDRESS, la textura se aplica tres veces en ambas direcciones u-y. Cada una de las demás filas y columnas a las que se aplica es una imagen reflejada de la fila o columna anterior, tal y como se muestra en la siguiente ilustración.

![Ilustración de imágenes reflejadas en una cuadrícula de 3x3](images/mirror.png)

Los efectos de este modo de dirección de textura son similares a los del modo de ajuste. Para obtener más información, vea [ajustar el modo de dirección de textura (Direct3D 9)](wrap-texture-address-mode.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
