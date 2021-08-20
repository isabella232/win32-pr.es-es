---
title: Registro de dependencias de aplicación (Reproductor de Windows Media SDK)
description: Obtenga información sobre cómo registrar la aplicación con componentes en tiempo de ejecución de las API proporcionadas por el SDK Reproductor de Windows Media.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Reproductor de Windows Media,application dependency registry settings
- Reproductor de Windows Media,configuración del Registro de dependencias
- Reproductor de Windows Media,registry
- registry,application dependency settings
- registry,dependency settings
- registry,settings for Reproductor de Windows Media
- configuración del registro de dependencias
- configuración del registro de dependencias de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa210debc4045326eb3bbae1e4fc137db5fb5a5dec6b89e493aedd54f110f82f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861555"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Registro de dependencias de aplicación (Reproductor de Windows Media SDK)

Las aplicaciones que usan las API proporcionadas por el SDK de Reproductor de Windows Media o Windows SDK de formato multimedia dependen de los componentes en tiempo de ejecución de esas tecnologías. Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.

Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente. Cuando se registra una o varias aplicaciones con una dependencia de bloqueo en uno de los componentes en tiempo de ejecución, se bloqueará el componente de una reversión a una versión anterior. Las aplicaciones dependientes que no están registradas como bloqueo no bloquean la reversión. En su lugar, antes de realizar la reversión, se muestra al usuario un mensaje que indica que las aplicaciones dependen del componente.

Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación. El valor del Registro que se va a establecer depende del componente del que depende la aplicación. También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.

Los siguientes valores del Registro se usan para registrar la dependencia en Reproductor de Windows Media runtime del SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Los siguientes valores del Registro se usan para registrar la dependencia en el entorno de ejecución Windows SDK de formato multimedia:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF TYPE \\ \\ *\_ Version,* \\ "*APP*", "*WMF \_ VERSION*"

Las siguientes variables se usan en los valores del Registro enumerados anteriormente:

*TIPO \_ REF*

Reemplace por BlockingRefCounts para bloquear la dependencia o por DependentRefCounts para la dependencia sin bloqueo.

*APP*

Nombre o descriptor corto de la aplicación. Esta cadena no se usará en los mensajes que se muestran para el usuario. Este valor es el identificador utilizado en los tres valores del Registro asociados a cada uno de los componentes en tiempo de ejecución.

*CADENA DE \_ APLICACIÓN*

Descriptor de la aplicación. Esta cadena se puede usar en los mensajes que se muestran para el usuario.

*DESCRIPTOR \_ DE REFERENCIA*

Descripción de cómo la aplicación usa el componente. Este valor puede incluir un máximo de 256 caracteres.

*VERSIÓN DE \_ WMP*

Versión de Reproductor de Windows Media requiere la aplicación. Si no se especifica ninguna versión, se supone que el valor predeterminado es 9.0.0.0.

*VERSIÓN DE \_ WMF*

Versión del SDK Windows Media Format requerido por la aplicación.

Los tres valores del Registro de ejemplo siguientes muestran cómo configurar los valores de la aplicación:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "Southplayer Video Player"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Descriptor, "Southvideo", "Southplayer Video Player uses the Windows Media Format SDK to play video files".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




