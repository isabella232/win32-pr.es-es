---
title: Acerca de los objetos Cdrom y CdromCollection
description: Acerca de los objetos Cdrom y CdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Reproductor de Windows Media, objeto Cdrom
- Reproductor de Windows Media modelo de objetos, objeto Cdrom
- object model,Cdrom object
- Reproductor de Windows Media ActiveX control, objeto Cdrom
- ActiveX control, objeto Cdrom
- Reproductor de Windows Media Control ActiveX móvil, objeto Cdrom
- Reproductor de Windows Media Mobile, objeto Cdrom
- Objeto Cdrom
- Reproductor de Windows Media, objeto CdromCollection
- Reproductor de Windows Media de objetos, objeto CdromCollection
- object model,CdromCollection object
- Reproductor de Windows Media ActiveX control, objeto CdromCollection
- ActiveX control, objeto CdromCollection
- Reproductor de Windows Media Control ActiveX móvil, objeto CdromCollection
- Reproductor de Windows Media Objeto Mobile,CdromCollection
- CdromCollection, objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264820"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>Acerca de los objetos Cdrom y CdromCollection

Los **objetos Cdrom** y **CdromCollection** rigen la interfaz de las unidades de CD del equipo con fines de lectura y reproducción de CDs.

Solo se tiene acceso al objeto **CdromCollection** a través de la **propiedad cdromCollection** del **objeto Player.** La **propiedad cdromCollection** devuelve el **objeto CdromCollection.** Solo puede acceder a las propiedades del **objeto CdromCollection** después de crearlo. Por ejemplo, para usar la **propiedad count,** debe usar el código siguiente:


```C++
mycount = player.cdromcollection.count;
```



Solo puede acceder al objeto **Cdrom** a través del **objeto CdromCollection.** Por ejemplo, para expulsar el CD mediante el método **De expulsión,** primero debe crear el objeto de colección y, a continuación, un elemento en el objeto . Para expulsar el CD, use el código siguiente:


```C++
player.cdromcollection.item(0).eject();
```



En ambos casos, primero va a crear el objeto de colección (**CdromCollection**) y, después, a obtener un objeto específico de esa colección. El objeto es el primer elemento de la colección, **Item**(0), que corresponde a la primera unidad de CD. A continuación, llame a un **método, Expulsión,** en ese elemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**CdromCollection (objeto)**](cdromcollection-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




