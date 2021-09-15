---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Reproductor de Windows Media,protocolos
- Reproductor de Windows Media de objetos, protocolos
- object model,protocols
- Reproductor de Windows Media ActiveX control,protocolos para el modelo de objetos
- ActiveX control,protocolos para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móviles, protocolos para el modelo de objetos
- Reproductor de Windows Media Móvil, protocolos para el modelo de objetos
- protocolos, Reproductor de Windows Media de objetos
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579385"
---
# <a name="wmpcd-protocol"></a>Protocolo WMPCD

El protocolo WMPCD permite especificar pistas en un disco compacto mediante la sintaxis url. Esta es la sintaxis general del protocolo:


```C++
wmpcd://drive/track
```



El *segmento de* unidad es el índice de la unidad de CD. El *segmento* de pista es el número de la pista. En el ejemplo siguiente se muestra cómo usar el protocolo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



En el ejemplo se reproduce la cuarta pista en el disco de la primera unidad de CD (la unidad cuyo índice es 0).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Protocolos y tipos de archivo admitidos**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




