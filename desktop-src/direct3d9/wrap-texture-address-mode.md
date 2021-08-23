---
description: El modo de dirección de textura de encapsulado, identificado por el miembro D3DTADDRESS WRAP del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D repita la textura en cada unión \_ de entero.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modo de dirección de textura encapsulada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820273a68754c11f17f4f2762c7e824562b8e52bfc0b2b097c21e82789ce4168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627834"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Modo de dirección de textura encapsulada (Direct3D 9)

El modo de dirección de textura de encapsulado, identificado por el miembro D3DTADDRESS WRAP del tipo enumerado \_ [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) hace que Direct3D repita la textura en cada unión de entero. Supongamos, por ejemplo, que la aplicación crea una primitiva cuadrada y especifica las coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) y (3.0,0.0). Al establecer el modo de direccionamiento de textura en D3DTADDRESS WRAP, la textura se aplica tres veces en las direcciones u y v, como se muestra en la \_ ilustración siguiente.

![ilustración de una textura de cara encapsulada en la dirección U y la dirección V](images/wrap.png)

Los efectos de este modo de dirección de textura son similares, pero distintos de los del modo reflejado. Para obtener más información, vea [Mirror Texture Address Mode (Direct3D 9) (Modo de dirección de textura de reflejo [Direct3D 9]).](mirror-texture-address-mode.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
