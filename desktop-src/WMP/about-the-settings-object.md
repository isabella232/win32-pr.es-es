---
title: Acerca del objeto de configuración
description: Acerca del objeto de configuración
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Media Player de Windows, objeto de configuración
- Modelo de objetos de Windows Media Player, objeto de configuración
- modelo de objetos, objeto de configuración
- Control ActiveX de Windows Media Player, objeto de configuración
- Control ActiveX, objeto Settings
- Control ActiveX móvil de Windows Media Player, objeto de configuración
- Windows Media Player Mobile, objeto de configuración
- Objeto de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903186"
---
# <a name="about-the-settings-object"></a>Acerca del objeto de configuración

El objeto de **configuración** rige los valores del control, como el volumen, el recuento de reproducción, el silencia, etc. Solo se tiene acceso a ella a través de la propiedad **Settings** del objeto **Player** . La propiedad **Settings** devuelve el objeto de **configuración** . Solo se puede tener acceso a las propiedades del objeto de **configuración** después de que se haya creado. Por ejemplo, para obtener el valor de la propiedad **Volume** , debe usar el código siguiente:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 




