---
title: Acerca del objeto de red
description: Acerca del objeto de red
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Reproductor de Windows Media,objeto Network
- Reproductor de Windows Media modelo de objetos, objeto Network
- object model,Network object
- Reproductor de Windows Media ActiveX control, objeto Network
- ActiveX control, objeto Network
- Reproductor de Windows Media Control de ActiveX móvil, objeto Network
- Reproductor de Windows Media Mobile,Network , objeto
- Objeto de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890260"
---
# <a name="about-the-network-object"></a>Acerca del objeto de red

El **objeto Network** rige las propiedades que permiten determinar el nivel de streaming del contenido a través de la red. Por ejemplo, puede averiguar si los paquetes se pierden y tomar las medidas adecuadas. Solo **se tiene** acceso al objeto Network a través de la propiedad **de** red del **objeto Player.** La **propiedad de** red devuelve el objeto **Network.** Solo puede acceder a las propiedades del **objeto Network** después de crearlo. Por ejemplo, para usar la **propiedad Bandwidth,** debe usar el código siguiente:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




