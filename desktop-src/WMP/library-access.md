---
title: Acceso a la biblioteca
description: Acceso a la biblioteca
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos, biblioteca
- object model,library
- Reproductor de Windows Media Móvil, biblioteca para el modelo de objetos
- Reproductor de Windows Media ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil, biblioteca para el modelo de objetos
- ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media biblioteca, acceso
- library,accessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01488a792f52c8602f18db22f195c32aa36069c50f363c16e405f3ddf2fd710a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617305"
---
# <a name="library-access"></a>Acceso a la biblioteca

Las propiedades y métodos del Reproductor de Windows Media de objetos que tienen acceso a la biblioteca requieren acceso de solo lectura o de lectura/escritura a la base de datos. La biblioteca contiene información que algunos usuarios quieren mantener privada y a la que solo se debe acceder o modificar con su consentimiento.

Para Reproductor de Windows Media serie 9 o posterior, puede determinar mediante programación el nivel de acceso. Para determinar el nivel actual de acceso concedido al código, recupere el *Configuración*. **propiedad mediaAccessRights.** Esa propiedad devuelve "none", "read" o "full" (lectura/escritura). Para solicitar derechos de acceso específicos, llame al *Configuración*. **Método requestMediaAccessRights,** pasando un parámetro que especifica el nivel que está solicitando. El método muestra un mensaje al usuario que explica el nivel de acceso solicitado y devuelve un **valor booleano** que indica si se concedió el acceso.

Determinados derechos de acceso se conceden automáticamente en función de dónde se ejecute el código en relación con el equipo del usuario.

-   Si la página web o el programa se encuentran en el equipo del usuario, se conceden derechos de acceso completos de forma predeterminada.
-   Las páginas web tienen acceso de lectura al *Reproductor de*. **currentMedia**, *Player*. **currentPlaylist** y *Media*. **sourceURL** cuando la página web se encuentra en una zona de seguridad de Internet Explorer que es igual o menos restringida que la zona de seguridad del elemento multimedia o lista de reproducción.

    Desde la zona menos restringida hasta la más  restringida, las zonas de seguridad son la zona de confianza (incluido el equipo local del usuario), la zona **intranet** local, la zona **de Internet** y la **zona** restringida.

    Por ejemplo, una página web de la **zona intranet local** tiene derechos de acceso completos al *reproductor*. **currentMedia** cuando el elemento multimedia correspondiente está en la intranet local o en Internet, pero se deben solicitar derechos de acceso para los elementos multimedia ubicados en el equipo local de un usuario o en un sitio web de la **zona** de confianza.

Debe probar la aplicación basada en web Windows en todas las zonas de seguridad que pueda encontrar. La aplicación debe diseñarse para controlar correctamente la denegación de una solicitud de acceso.

Reproductor de Windows Media versiones del modelo de objetos anteriores a Reproductor de Windows Media serie 9 no incluyen **mediaAccessRights** ni **requestMediaAccessRights**. Estas versiones anteriores de Reproductor de Windows Media permiten al usuario establecer niveles de acceso mediante el **cuadro de diálogo** Opciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




