---
description: El modo de dirección de textura de encapsulado, identificado por el \_ miembro D3DTADDRESS Wrap del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D repita la textura en cada unión de enteros.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Ajustar el modo de dirección de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274644"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Ajustar el modo de dirección de textura (Direct3D 9)

El modo de dirección de textura de encapsulado, identificado por el \_ miembro D3DTADDRESS Wrap del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D repita la textura en cada unión de enteros. Supongamos, por ejemplo, que la aplicación crea un primitivo cuadrado y especifica las coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0). Al establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Wrap, la textura se aplica tres veces en las direcciones u-y v, tal como se muestra en la siguiente ilustración.

![Ilustración de una textura de caras ajustada en la dirección u y en la dirección de v](images/wrap.png)

Los efectos de este modo de dirección de textura son similares a los del modo de reflejo. Para obtener más información, vea [modo de dirección de textura de reflejo (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
