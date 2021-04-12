---
title: Acceso a bibliotecas
description: Acceso a bibliotecas
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, acceso
- Biblioteca, acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357072"
---
# <a name="library-access"></a>Acceso a bibliotecas

Las propiedades y los métodos del modelo de objetos de Media Player de Windows que tienen acceso a la biblioteca requieren acceso de solo lectura o de lectura y escritura a la base de datos. La biblioteca contiene información que algunos usuarios quieren mantener privados y a los que se debe tener acceso o modificar solo con su consentimiento.

En Windows Media Player serie 9 o posterior, puede determinar mediante programación el nivel de acceso. Para determinar el nivel actual de acceso concedido al código, recupere la *configuración*. propiedad **mediaAccessRights** . Esa propiedad devuelve "none", "Read" o "Full" (lectura y escritura). Para solicitar derechos de acceso específicos, llame a la *configuración*. método **requestMediaAccessRights** , pasando un parámetro que especifica el nivel que se solicita. El método muestra un mensaje al usuario que explica el nivel de acceso solicitado y devuelve un valor **booleano** que indica si se ha concedido el acceso.

Determinados derechos de acceso se conceden automáticamente en función de dónde se ejecute el código en relación con el equipo del usuario.

-   Si la página web o el programa se encuentra en el equipo del usuario, se concederán derechos de acceso completo de forma predeterminada.
-   Las páginas web tienen acceso de lectura al *reproductor*. **currentMedia**, *reproductor*. **currentPlaylist** y *multimedia*. **sourceURL** cuando la página web se encuentra en una zona de seguridad de Internet Explorer que es igual o menos restringida que la zona de seguridad del elemento multimedia o de la lista de reproducción.

    En el intervalo de menos restringido a más restringido, las zonas de seguridad son la zona de **confianza** (incluido el equipo local del usuario), la zona de **Intranet local** , la zona de **Internet** y la zona **restringida** .

    Por ejemplo, una página web de la zona **Intranet local** tiene derechos de acceso completo al *reproductor*. **currentMedia** cuando el elemento multimedia correspondiente está en la Intranet local o en Internet, pero se deben solicitar derechos de acceso para los elementos multimedia ubicados en el equipo local de un usuario o en un sitio web de la zona de **confianza** .

Debe probar la aplicación basada en web o en Windows en todas las zonas de seguridad con las que puede encontrarse. La aplicación debe diseñarse para controlar la denegación de una solicitud de acceso correctamente.

Las versiones del modelo de objetos de Windows Media Player anteriores a Windows Media Player 9 no incluyen **mediaAccessRights** ni **requestMediaAccessRights**. Estas versiones anteriores de Windows Media Player permiten al usuario establecer niveles de acceso mediante el cuadro de diálogo **Opciones** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




