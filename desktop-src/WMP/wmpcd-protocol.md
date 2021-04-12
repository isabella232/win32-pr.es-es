---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolos
- Modelo de objetos de Windows Media Player, protocolos
- modelo de objetos, protocolos
- Control ActiveX de Windows Media Player, protocolos para el modelo de objetos
- Control ActiveX, protocolos para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, protocolos para el modelo de objetos
- Windows Media Player Mobile, protocolos para el modelo de objetos
- protocolos, modelo de objetos de Windows Media Player
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268724"
---
# <a name="wmpcd-protocol"></a>Protocolo WMPCD

El protocolo WMPCD le permite especificar pistas en un disco compacto mediante la sintaxis de la dirección URL. Esta es la sintaxis general del Protocolo:


```C++
wmpcd://drive/track
```



El segmento de la *unidad* es el índice de la unidad de CD. El segmento de *seguimiento* es el número de la pista. En el siguiente ejemplo se muestra el uso del protocolo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



En el ejemplo se reproduce la cuarta pista del disco en la primera unidad de CD (la unidad cuyo índice es 0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tipos de archivos y protocolos admitidos**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




