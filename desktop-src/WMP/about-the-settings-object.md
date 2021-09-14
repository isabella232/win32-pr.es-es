---
title: Acerca del objeto Configuración
description: Acerca del objeto Configuración
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Reproductor de Windows Media,Configuración objeto
- Reproductor de Windows Media modelo de objetos, Configuración objeto
- object model,Configuración object
- Reproductor de Windows Media ActiveX control, Configuración objeto
- ActiveX control, Configuración objeto
- Reproductor de Windows Media Control ActiveX móvil, Configuración objeto
- Reproductor de Windows Media Mobile,Configuración objeto
- Configuración objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967771"
---
# <a name="about-the-settings-object"></a>Acerca del objeto Configuración

El **Configuración** control controla la configuración del control, como el volumen, el recuento de reproducción, la exclusión mutua, y así sucesivamente. Solo se accede a él a través de **Configuración** propiedad del **objeto Player.** La **Configuración** devuelve el **Configuración** objeto . Solo puede acceder a las propiedades del **objeto Configuración** después de crearlo. Por ejemplo, para obtener el valor de la **propiedad Volume,** debe usar el código siguiente:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 




