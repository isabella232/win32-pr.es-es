---
title: Acerca del objeto de DVD
description: Acerca del objeto de DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Media Player de Windows, objeto de DVD
- Modelo de objetos de Windows Media Player, objeto de DVD
- modelo de objetos, objeto de DVD
- Control ActiveX de Windows Media Player, objeto de DVD
- Control ActiveX, objeto DVD
- Control ActiveX móvil de Windows Media Player, objeto de DVD
- Windows Media Player Mobile, objeto de DVD
- Objeto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356734"
---
# <a name="about-the-dvd-object"></a>Acerca del objeto de DVD

El objeto de **DVD** agrega funcionalidad específica de los medios de DVD. En general, los medios de DVD se tratan igual que otros medios digitales de Windows Media Player. Por ejemplo, las unidades de DVD se enumeran mediante el objeto **CdromCollection** y los títulos y capítulos de DVD se manipulan mediante objetos de **lista de reproducción** y objetos **multimedia** . Sin embargo, algunas funciones son específicas del DVD y el objeto de **DVD** lo proporciona. Por ejemplo, DVD tiene un concepto denominado dominio. Para recuperar el dominio actual para los medios de DVD, escriba lo siguiente:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




