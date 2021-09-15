---
title: Registro de dependencias de aplicación (Windows SDK de formato multimedia 11)
description: Obtenga información sobre cómo registrar la aplicación con los componentes en tiempo de ejecución de las API proporcionadas por el SDK Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows SDK de formato multimedia, registro de dependencias de aplicación
- registro de dependencias de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570217"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registro de dependencias de aplicación (Windows SDK de formato multimedia 11)

Las aplicaciones que usan las API proporcionadas por el SDK Windows Media Format o Reproductor de Windows Media SDK dependen de los componentes en tiempo de ejecución de esas tecnologías. Puede registrar la aplicación como dependiente de esos componentes como parte de la configuración de la aplicación.

Al registrar la aplicación, puede elegir uno de los dos niveles de dependencia: bloqueo o dependiente. Cuando una o varias aplicaciones se registran con una dependencia de bloqueo en uno de los componentes en tiempo de ejecución, se bloqueará el componente de una reversión a una versión anterior. Las aplicaciones dependientes que no están registradas como bloqueo, no bloquean la reversión. En su lugar, antes de realizar la reversión, se le pide al usuario un mensaje que indica que las aplicaciones dependen del componente.

Para registrar la aplicación, debe establecer un valor en el registro que identifique la aplicación. El valor del Registro que se va a establecer depende del componente del que depende la aplicación. También puede establecer dos valores adicionales por dependencia para proporcionar información adicional sobre la aplicación.

Los siguientes valores del Registro se usan para registrar la dependencia en el entorno Windows del SDK de formato multimedia:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF TYPE \\ \\ *\_ Version,* \\ "*APP*", "*WMF \_ VERSION*"

El siguiente valor del Registro se usa para registrar la dependencia de Reproductor de Windows Media runtime del SDK:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"

Las siguientes variables se usan en los valores del Registro enumerados anteriormente:

*TIPO \_ REF*

Reemplace por BlockingRefCounts para bloquear la dependencia o por DependentRefCounts para la dependencia sin bloqueo.

*APP*

Nombre o descriptor corto de la aplicación. Esta cadena no se usará en los mensajes que se muestran para el usuario. Este valor es el identificador utilizado en los tres valores del Registro asociados a cada uno de los componentes en tiempo de ejecución.

*CADENA DE \_ APLICACIÓN*

Descriptor de la aplicación. Esta cadena se puede usar en los mensajes que se muestran para el usuario.

*REF \_ DESCRIPTOR*

Descripción de cómo la aplicación usa el componente. Este valor puede incluir un máximo de 256 caracteres.

*VERSIÓN DE \_ WMP*

Versión de Reproductor de Windows Media requiere la aplicación.

*VERSIÓN DE \_ WMF*

Versión del SDK Windows Media Format requerido por la aplicación.

Los tres valores del Registro de ejemplo siguientes muestran cómo configurar los valores de la aplicación:

-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsConfiguración de \\ \\ MicrosoftMedia Aplicación DependentRefCounts, \\ "Southvideo", "Reproductor de vídeo de Southvideo"
-   HKEY CLASSES ROOT Software Microsoft WindowsConfiguración de MicrosoftMedia \_ \_ \\ \\ \\ \\ \\ DescriptorRefCounts, \\ "Southvideo", "Southvideo Video Player usa el SDK de formato multimedia de Windows para reproducir archivos de vídeo".
-   HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsConfiguración de \\ \\ MicrosoftMedia DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Project Consideraciones**](project-considerations.md)
</dt> </dl>

 

 




