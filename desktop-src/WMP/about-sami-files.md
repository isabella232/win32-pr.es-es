---
title: Acerca de los archivos SAMI
description: Acerca de los archivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903535"
---
# <a name="about-sami-files"></a>Acerca de los archivos SAMI

Los archivos SAMI son archivos de texto que tienen una extensión de nombre de archivo. SMI o. Sami. Contienen las cadenas de texto que se usan para subtítulos cerrados, subtítulos y descripciones de audio sincronizados. También especifican los parámetros de tiempo utilizados por el control de Media Player de Windows para sincronizar el texto de subtítulos con el contenido de audio o vídeo. Cuando un archivo multimedia digital alcanza una hora designada en el archivo SAMI, el texto cambia en consecuencia en el área de presentación de la leyenda cerrada de la Página Web.

Aparte de un simple editor de texto (como el Bloc de notas de Microsoft), no se requiere software especial para crear un archivo SAMI. SAMI y HTML comparten elementos comunes, como las <HEAD> etiquetas y <BODY> . Como en HTML, las etiquetas utilizadas en los archivos SAMI siempre deben usarse en pares. Por ejemplo, un elemento BODY comienza con una <BODY> etiqueta y siempre debe terminar con una </BODY> etiqueta.

Un archivo SAMI básico requiere tres etiquetas fundamentales: <SAMI> , <HEAD> y <BODY> .

La <SAMI> etiqueta identifica el documento como un documento Sami para que otras aplicaciones puedan reconocer su formato de archivo.

Entre las etiquetas <HEAD> y </HEAD> , se definen las instrucciones básicas y otra información de formato para el documento Sami, como el título del documento, la información general y las propiedades de estilo de los subtítulos (CC). Como HTML, el contenido declarado en el elemento de encabezado no se muestra como salida.

Los elementos y atributos definidos entre las etiquetas <BODY> y </BODY> muestran el contenido que el usuario ha visualizado. En SAMI, el elemento BODY contiene los parámetros para la sincronización y las cadenas de texto que se usan para los subtítulos cerrados.

Definido en el elemento de encabezado, el elemento de estilo proporciona la funcionalidad agregada en SAMI. Entre las etiquetas <STYLE> y </STYLE> , puede definir varios selectores de hoja de estilos en cascada (CSS) para el estilo y el diseño. Las propiedades de estilo, como las fuentes, los tamaños y las alineaciones, se pueden personalizar para proporcionar una experiencia de usuario enriquecida, al tiempo que se fomenta la accesibilidad. Por ejemplo, la definición de una clase de estilo de fuente de texto grande puede mejorar la legibilidad de los usuarios que tienen dificultades para leer texto pequeño. Además, al definir varias clases de lenguaje diferentes, puede ayudar a los usuarios internacionales a entender mejor el contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




