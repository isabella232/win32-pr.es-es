---
title: Acerca del objeto de red
description: Acerca del objeto de red
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Media Player de Windows, objeto de red
- Modelo de objetos de Windows Media Player, objeto de red
- modelo de objetos, objeto de red
- Control ActiveX de Windows Media Player, objeto de red
- Control ActiveX, objeto de red
- Control ActiveX móvil de Windows Media Player, objeto de red
- Windows Media Player Mobile, objeto de red
- Objeto de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773338"
---
# <a name="about-the-network-object"></a>Acerca del objeto de red

El objeto de **red** rige las propiedades que le permiten determinar la forma en que el contenido se transmite por secuencias a través de la red. Por ejemplo, puede averiguar si los paquetes se están perdido y tomar las medidas adecuadas. Solo se tiene acceso al objeto de **red** a través de la propiedad **Network** del objeto **Player** . La propiedad de **red** devuelve el objeto de **red** . Solo puede acceder a las propiedades del objeto de **red** una vez creado. Por ejemplo, para utilizar la propiedad **ancho de banda** , debe usar el código siguiente:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




