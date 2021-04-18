---
title: Ocultar el control Media Player de Windows
description: Ocultar el control Media Player de Windows
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- incrustación, páginas web
- Windows Media Player, ocultar el control ActiveX
- Modelo de objetos de Windows Media Player, ocultar el control ActiveX
- modelo de objetos, ocultar control ActiveX
- Windows Media Player Mobile, control hidingActiveX
- Control ActiveX de Windows Media Player, ocultar
- Control ActiveX móvil de Windows Media Player, ocultar
- Control ActiveX, ocultar
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Incrustación de páginas web, ocultar controles ActiveX
- ocultar Windows Media Player control ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357467"
---
# <a name="hiding-the-windows-media-player-control"></a>Ocultar el control Media Player de Windows

El objeto de Windows Media Player ActiveX se incrusta en una página web mediante el elemento de objeto. A diferencia de las versiones anteriores, el elemento de objeto que define Windows Media Player debe colocarse en la sección de cuerpo de una página web, entre las etiquetas <BODY> y </BODY> . Colocar el objeto de Windows Media Player ActiveX en la sección de encabezado de una página web para ocultar la interfaz de usuario puede producir resultados inesperados.

Si coloca el control ActiveX de Windows Media Player en la sección de cuerpo de una página web, se mostrará la interfaz de usuario del control. Si no desea que se muestre y desea crear su propia interfaz de usuario, establezca los atributos de alto y ancho del elemento de objeto en cero.

El control también se puede hacer invisible si se establece el *reproductor*. propiedad **uiMode** en "invisible". Esto puede hacerse mediante una etiqueta PARAM, como se describe en la sección siguiente. En este caso, el espacio se reserva para el control con el alto y el ancho, pero no se muestra nada en el espacio reservado hasta que **uiMode** se cambie a un valor distinto de "invisible".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Media Player de Windows en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




