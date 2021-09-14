---
title: Acerca del objeto DVD
description: Acerca del objeto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Reproductor de Windows Media,OBJETO DVD
- Reproductor de Windows Media modelo de objetos, objeto DVD
- object model,DVD object
- Reproductor de Windows Media ActiveX control,objeto DVD
- ActiveX control,objeto DVD
- Reproductor de Windows Media Control de ActiveX móvil,objeto DVD
- Reproductor de Windows Media Objeto Mobile,DVD
- Objeto DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264767"
---
# <a name="about-the-dvd-object"></a>Acerca del objeto DVD

El **objeto DVD** agrega funcionalidad específica a los medios de DVD. En un sentido general, los medios de DVD se tratan igual que otros medios digitales en Reproductor de Windows Media. Por ejemplo, las unidades de DVD se enumeran mediante el objeto **CdromCollection** y los títulos de DVD y los capítulos se manipulan mediante objetos **De** lista de reproducción y **Objetos** multimedia. Sin embargo, algunas funcionalidades son específicas de DVD y el **objeto DVD** lo proporciona. Por ejemplo, DVD tiene un concepto denominado dominio. Para recuperar el dominio actual para los medios de DVD, escriba lo siguiente:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto DVD**](dvd-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




