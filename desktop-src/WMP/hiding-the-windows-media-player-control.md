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
- control Reproductor de Windows Media ActiveX,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- control ActiveX,Páginas web
- embedding,Web pages
- Reproductor de Windows Media, ocultar ActiveX control
- Reproductor de Windows Media de objetos, ocultar ActiveX control
- modelo de objetos, ocultar ActiveX control
- Reproductor de Windows Media Mobile,hidingActiveX control
- Reproductor de Windows Media ActiveX control, ocultar
- Reproductor de Windows Media Control de ActiveX móvil, ocultar
- ActiveX control, ocultar
- control Reproductor de Windows Media ActiveX,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- control ActiveX,Páginas web
- Inserción de páginas web, ocultar ActiveX control
- ocultar Reproductor de Windows Media ActiveX control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7c25f75538f1e20a08ef252b20212df48a565
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882271"
---
# <a name="hiding-the-windows-media-player-control"></a>Ocultar el control Reproductor de Windows Media control

El Reproductor de Windows Media ActiveX objeto se inserta en una página web mediante el elemento OBJECT. A diferencia de las versiones anteriores, el elemento OBJECT que define Reproductor de Windows Media debe colocarse en la sección BODY de una página web, entre &lt; BODY &gt; y </BODY> Etiquetas. Colocar el Reproductor de Windows Media ActiveX en la sección HEAD de una página web para ocultar la interfaz de usuario puede producir resultados inesperados.

Si coloca el control Reproductor de Windows Media ActiveX en la sección CUERPO de una página web, se mostrará la interfaz de usuario del control. Si no desea que se muestre y desea crear su propia interfaz de usuario, establezca los atributos de alto y ancho del elemento OBJECT en cero.

El control también se puede hacer invisible estableciendo el *reproductor*. **Propiedad uiMode** a "invisible". Esto se puede hacer mediante una etiqueta PARAM como se describe en la sección siguiente. En este caso, el espacio se reserva para el control mediante el alto y el ancho, pero no se muestra nada en el espacio reservado hasta que **uiMode** se cambia a algo distinto de "invisible".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Reproductor de Windows Media en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




