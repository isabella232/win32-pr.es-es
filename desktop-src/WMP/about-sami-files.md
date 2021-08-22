---
title: Acerca de los archivos SAMI
description: Acerca de los archivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media modelo de objetos, Intercambio multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- Reproductor de Windows Media ActiveX control, Intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Control ActiveX dispositivos móviles, Intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control,Intercambio multimedia accesible sincronizado (SAMI)
- Intercambio multimedia accesible sincronizado (SAMI),files
- SAMI (intercambio multimedia accesible sincronizado), archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcb4823ee02a501254218a9b7c4d9aaf347894d895bc193c8ce763658db174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470465"
---
# <a name="about-sami-files"></a>Acerca de los archivos SAMI

Los archivos SAMI son archivos de texto que tienen una extensión de nombre de archivo .smi o .sami. Contienen las cadenas de texto que se usan para los subtítulos, subtítulos y descripciones de audio sincronizados. También especifican los parámetros de control de tiempo utilizados por el control Reproductor de Windows Media sincronizar el texto de subtítulos con contenido de audio o vídeo. Cuando un archivo multimedia digital alcanza una hora designada en el archivo SAMI, el texto cambia en consecuencia en el área de presentación de subtítulos de la página web.

Aparte de un editor de texto simple (como Microsoft Bloc de notas), no se necesita software especial para crear un archivo SAMI. SAMI y HTML comparten elementos comunes, como <HEAD> y <BODY> Etiquetas. Al igual que en HTML, las etiquetas usadas en archivos SAMI siempre se deben usar en pares. Por ejemplo, un elemento BODY comienza con un <BODY> tag y siempre deben terminar con un </BODY> .

Un archivo SAMI básico requiere tres etiquetas fundamentales: <SAMI> , <HEAD>e <BODY>.

La <SAMI> etiqueta identifica el documento como un documento SAMI para que otras aplicaciones puedan reconocer su formato de archivo.

Entre <HEAD> y </HEAD> etiquetas, defina directrices básicas y otra información de formato para el documento SAMI, como el título del documento, la información general y las propiedades de estilo de los títulos cerrados. Al igual que HTML, el contenido declarado dentro del elemento HEAD no se muestra como salida.

Elementos y atributos definidos entre <BODY> y </BODY> Las etiquetas muestran el contenido visto por el usuario. En SAMI, el elemento BODY contiene los parámetros para la sincronización y las cadenas de texto usadas para los títulos cerrados.

Definido dentro del elemento HEAD, el elemento STYLE proporciona funcionalidad agregada en SAMI. Entre las <STYLE> etiquetas y </STYLE> , puede definir varios selectores de hoja de estilos en cascada (CSS) para el estilo y el diseño. Las propiedades de estilo, como fuentes, tamaños y alineaciones, se pueden personalizar para proporcionar una experiencia de usuario enriquez al tiempo que se promueve la accesibilidad. Por ejemplo, definir una clase de estilo de fuente de texto grande puede mejorar la legibilidad de los usuarios que tienen dificultades para leer texto pequeño. Además, al definir varias clases de lenguaje diferentes, puede ayudar a los usuarios internacionales a comprender mejor el contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




