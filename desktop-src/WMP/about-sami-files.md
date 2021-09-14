---
title: Acerca de los archivos SAMI
description: Acerca de los archivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media de objetos, Intercambio de medios accesibles sincronizado (SAMI)
- object model,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- control Reproductor de Windows Media ActiveX, Intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Control de ActiveX móviles, intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control, Intercambio de medios accesibles sincronizado (SAMI)
- Intercambio multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio multimedia accesible sincronizado), archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f03d3e4079a117831ed8afb53648abf6a128ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264831"
---
# <a name="about-sami-files"></a>Acerca de los archivos SAMI

Los archivos SAMI son archivos de texto que tienen una extensión de nombre de archivo .smi o .sami. Contienen las cadenas de texto usadas para los subtítulos, subtítulos y descripciones de audio sincronizados. También especifican los parámetros de tiempo utilizados por el control Reproductor de Windows Media para sincronizar el texto de subtítulos con contenido de audio o vídeo. Cuando un archivo multimedia digital alcanza un tiempo designado en el archivo SAMI, el texto cambia en consecuencia en el área de presentación de subtítulos de la página web.

Aparte de un editor de texto simple (como Microsoft Bloc de notas), no se requiere software especial para crear un archivo SAMI. SAMI y HTML comparten elementos comunes, como <HEAD> y &lt; &gt; etiquetas BODY. Al igual que en HTML, las etiquetas usadas en archivos SAMI siempre deben usarse en pares. Por ejemplo, un elemento BODY comienza con una &lt; etiqueta BODY y siempre debe terminar con una etiqueta &gt; &lt; &gt; /BODY.

Un archivo SAMI básico requiere tres etiquetas fundamentales: &lt; SAMI &gt; , <HEAD>, y &lt; BODY &gt; .

La &lt; etiqueta SAMI &gt; identifica el documento como un documento SAMI para que otras aplicaciones puedan reconocer su formato de archivo.

Entre el <HEAD> y </HEAD> Etiquetas, defina directrices básicas y otra información de formato para el documento SAMI, como el título del documento, la información general y las propiedades de estilo de los títulos cerrados. Al igual que HTML, el contenido declarado dentro del elemento HEAD no se muestra como salida.

Los elementos y atributos definidos entre las etiquetas BODY y &lt; &gt; &lt; /BODY &gt; muestran el contenido que ve el usuario. En SAMI, el elemento BODY contiene los parámetros para la sincronización y las cadenas de texto usadas para los subtítulos.

Definido dentro del elemento HEAD, el elemento STYLE proporciona funcionalidad adicional en SAMI. Entre style y etiquetas, puede definir varios selectores de hoja de estilos en &lt; &gt; cascada </STYLE> (CSS) para el estilo y el diseño. Las propiedades de estilo, como fuentes, tamaños y alineaciones, se pueden personalizar para proporcionar una experiencia de usuario enriqueciendo al mismo tiempo que se promueve la accesibilidad. Por ejemplo, definir una clase de estilo de fuente de texto grande puede mejorar la legibilidad de los usuarios que tienen dificultades para leer texto pequeño. Además, al definir varias clases de lenguaje diferentes, puede ayudar a los usuarios internacionales a comprender mejor el contenido multimedia digital.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




