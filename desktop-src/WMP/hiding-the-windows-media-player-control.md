---
title: Ocultar el control Reproductor de Windows Media control
description: Ocultar el control Reproductor de Windows Media control
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media ActiveX control,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- ActiveX control,Páginas web
- embedding,Web pages
- Reproductor de Windows Media, ocultar ActiveX control
- Reproductor de Windows Media de objetos, ocultar ActiveX control
- modelo de objetos, ocultar ActiveX control
- Reproductor de Windows Media Control Mobile,hidingActiveX
- Reproductor de Windows Media ActiveX control, ocultar
- Reproductor de Windows Media Control de ActiveX móvil, ocultar
- ActiveX control, ocultar
- Reproductor de Windows Media ActiveX control,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- ActiveX control,Páginas web
- Inserción de páginas web, ocultar ActiveX control
- ocultar Reproductor de Windows Media ActiveX control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb0b29bbbc1b2eb978c5bd9f29a58aa02bf629d5c6befe9f1dc68bbc92d280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339186"
---
# <a name="hiding-the-windows-media-player-control"></a>Ocultar el control Reproductor de Windows Media control

El Reproductor de Windows Media ActiveX objeto se inserta en una página web mediante el elemento OBJECT. A diferencia de las versiones anteriores, el elemento OBJECT que Reproductor de Windows Media debe colocarse en la sección BODY de una página web, entre <BODY> y </BODY> Etiquetas. Colocar el Reproductor de Windows Media ActiveX en la sección HEAD de una página web para ocultar la interfaz de usuario puede producir resultados inesperados.

Si coloca el control Reproductor de Windows Media ActiveX en la sección CUERPO de una página web, se mostrará la interfaz de usuario del control. Si no desea que se muestre y desea crear su propia interfaz de usuario, establezca los atributos de alto y ancho del elemento OBJECT en cero.

El control también se puede hacer invisible estableciendo el *reproductor*. **Propiedad uiMode** en "invisible". Esto se puede hacer mediante una etiqueta PARAM como se describe en la sección siguiente. En este caso, el espacio se reserva para el control mediante el alto y el ancho, pero no se muestra nada en el espacio reservado hasta que **uiMode** se cambia a algo distinto de "invisible".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Reproductor de Windows Media en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




