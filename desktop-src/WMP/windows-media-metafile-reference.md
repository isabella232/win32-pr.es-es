---
title: Referencia de metarchivos de Windows Media
description: Referencia de metarchivos de Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metaarchivos de Windows Media, referencia
- metaarchivos, referencia
- referencia de los metaarchivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075686"
---
# <a name="windows-media-metafile-reference"></a>Referencia de metarchivos de Windows Media

Esta referencia documenta elementos y extensiones de nombre de archivo para los metaarchivos de Windows Media. La referencia se divide en las secciones siguientes.



| Sección                                                                                    | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Referencia de elementos de metarchivo de Windows Media](windows-media-metafile-elements-reference.md) | Documenta los elementos de metarchivo, incluidas las definiciones, los atributos y sus valores, y las condiciones especiales relacionadas con cada elemento. |
| [Extensiones de nombre de archivo](file-name-extensions.md)                                           | Documenta las extensiones de nombre de archivo de metarchivo con reglas e instrucciones sobre su uso.                                                  |



 

Los metaarchivos de Windows Media son archivos de texto que proporcionan información acerca de una secuencia de archivos y su presentación. Los metaarchivos se basan en la sintaxis de lenguaje de marcado extensible (XML) y se componen de varios elementos similares a XML con sus etiquetas y atributos. Cada elemento define una configuración o una acción para el streaming multimedia.

Hay dos conjuntos de etiquetas de elementos disponibles para los metaarchivos. Los metaarchivos del lado cliente tienen un conjunto de elementos y los metaarchivos del servidor tienen otro conjunto de elementos.

Si una etiqueta de elemento no tiene ningún elemento secundario (los que modifican o están contenidos en otro elemento), se puede usar un carácter de barra diagonal (/) al final de la etiqueta de apertura en lugar de una etiqueta de cierre. Si los elementos secundarios no aparecen entre la etiqueta de apertura y cierre de un elemento, no son elementos secundarios de ese elemento y se omiten o causan un error en la sintaxis del metarchivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los metaarchivos de Windows Media**](about-windows-media-metafiles.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Metaarchivos de Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




