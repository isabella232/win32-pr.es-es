---
title: Acerca de los objetos CDROM y CdromCollection
description: Acerca de los objetos CDROM y CdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Media Player de Windows, objeto CDROM
- Modelo de objetos de Windows Media Player, objeto CDROM
- modelo de objetos, CDROM (objeto)
- Control ActiveX de Windows Media Player, objeto CDROM
- Control ActiveX, CDROM (objeto)
- Control ActiveX móvil de Windows Media Player, objeto CDROM
- Windows Media Player Mobile, objeto CDROM
- CDROM (objeto)
- Media Player de Windows, objeto CdromCollection
- Modelo de objetos de Media Player de Windows, objeto CdromCollection
- modelo de objetos, CdromCollection (objeto)
- Control ActiveX de Windows Media Player, objeto CdromCollection
- Control ActiveX, objeto CdromCollection
- Control ActiveX de Windows Media Player Mobile, objeto CdromCollection
- Windows Media Player Mobile, objeto CdromCollection
- Objeto CdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776938"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>Acerca de los objetos CDROM y CdromCollection

Los objetos **CDROM** y **CdromCollection** rigen la interfaz a las unidades de CD del equipo con el fin de leer y reproducir CDs.

Solo se tiene acceso al objeto **CdromCollection** a través de la propiedad **CdromCollection** del objeto **Player** . La propiedad **cdromCollection** devuelve el objeto **cdromCollection** . Solo puede acceder a las propiedades del objeto **CdromCollection** una vez creado. Por ejemplo, para utilizar la propiedad **Count** , debe usar el código siguiente:


```C++
mycount = player.cdromcollection.count;
```



Solo puede acceder al objeto **CDROM** a través del objeto **CdromCollection** . Por ejemplo, para expulsar el CD con el método **EJECT** , primero debe crear el objeto de colección y, a continuación, un elemento en el objeto. Para expulsar el CD, use el siguiente código:


```C++
player.cdromcollection.item(0).eject();
```



En ambos casos, primero se crea el objeto de colección (**CdromCollection**) y, a continuación, se obtiene un objeto específico de esa colección. El objeto es el primer elemento de la colección, **Item**(0), que corresponde a la primera unidad de CD. A continuación, llame a un método, **EJECT**, en ese elemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




