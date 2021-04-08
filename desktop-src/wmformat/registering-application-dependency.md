---
title: Registrar la dependencia de la aplicación (Windows Media Format 11 SDK)
description: Registrando la dependencia de la aplicación
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- SDK de Windows Media Format, registrar dependencias de aplicaciones
- registrar las dependencias de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078678"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrar la dependencia de la aplicación (Windows Media Format 11 SDK)

Las aplicaciones que usan las API proporcionadas por el SDK de Windows Media Format o Windows Media Player SDK dependen de los componentes en tiempo de ejecución de esas tecnologías. Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.

Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente. Cuando una o varias aplicaciones se registran con una dependencia de bloqueo en uno de los componentes de tiempo de ejecución, el componente se bloqueará de una reversión a una versión anterior. Las aplicaciones dependientes que no están registradas como bloqueo, no bloquean la reversión. En su lugar, antes de que se lleve a cabo la reversión, se muestra al usuario un mensaje que indica que las aplicaciones dependen del componente.

Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación. El valor del registro que se va a establecer depende del componente del que dependa la aplicación. También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.

Los siguientes valores del registro se utilizan para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Format:

-   HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ tipo* \\ de la aplicación, "*aplicación*", "*\_ cadena de aplicación*"
-   HKEY \_ classes \_ \\ software raíz \\ Microsoft \\ windowsmedia \\ setup \\ descriptor de *\_ tipo REF* \\ , "*App*", "*ref \_ descriptor*"
-   HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ windowsmedia \\ setup \\ *ref \_ Type* \\ version, "*App*", "*WMF \_ version*"

El siguiente valor del registro se usa para registrar la dependencia del tiempo de ejecución del SDK de Windows Media Player:

-   HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ de aplicación, "*aplicación*", "*\_ cadena de aplicación*"
-   HKEY \_ clases \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ configuración \\ *ref \_* \\ descriptor de tipo, "*App*", "*ref \_ descriptor*"
-   HKEY \_ classes \_ raíz \\ software \\ Microsoft \\ MediaPlayer \\ setup \\ *ref \_ tipo* \\ version, "*App*", "*WMP \_ version*"

Las siguientes variables se usan en los valores del registro enumerados anteriormente:

*tipo de referencia \_*

Reemplazar por BlockingRefCounts para la dependencia de bloqueo o con DependentRefCounts para la dependencia sin bloqueo.

*APP*

Nombre o descriptor corto de la aplicación. Esta cadena no se utilizará en los mensajes mostrados para el usuario. Este valor es el identificador que se usa en los tres valores del registro asociados a cada uno de los componentes en tiempo de ejecución.

*cadena de aplicación \_*

Descriptor de la aplicación. Esta cadena se puede usar en los mensajes mostrados para el usuario.

*descriptor de referencia \_*

Descripción del modo en que la aplicación usa el componente. Este valor puede incluir un máximo de 256 caracteres.

*versión de WMP \_*

Versión de Windows Media Player requerida por la aplicación.

*\_versión WMF*

Versión del SDK de Windows Media Format que requiere la aplicación.

En los siguientes tres valores del registro de ejemplo se muestra cómo configurar los valores de la aplicación:

-   HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"
-   HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ descriptor, "SouthridgeVideo", "Southridge Video Player usa el SDK de Windows Media Format para reproducir archivos de vídeo".
-   HKEY \_ classes \_ root \\ software \\ Microsoft \\ windowsmedia \\ setup \\ DependentRefCounts \\ version, "SouthridgeVideo", "9.0.0.2600"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Consideraciones del proyecto**](project-considerations.md)
</dt> </dl>

 

 




