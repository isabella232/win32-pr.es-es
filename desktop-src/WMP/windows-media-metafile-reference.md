---
title: Windows Referencia de metarchivo multimedia
description: Windows Referencia de metarchivo multimedia
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Metarchivos multimedia,referencia
- metarchivos, referencia
- Referencia de metarchivos Windows multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b00cd604ec94c42ef90f08a8875edb4fda92ba8267c7e4a7d7b5505c2fb57932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862265"
---
# <a name="windows-media-metafile-reference"></a>Windows Referencia de metarchivo multimedia

Esta referencia documenta los elementos y las extensiones de nombre de archivo Windows metarchivos multimedia. La referencia se divide en las secciones siguientes.



| Sección                                                                                    | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Referencia de elementos de metarchivo multimedia](windows-media-metafile-elements-reference.md) | Documenta los elementos de metarchivo, incluidas las definiciones, los atributos y sus valores, y las condiciones especiales relacionadas con cada elemento. |
| [Extensiones de nombre de archivo](file-name-extensions.md)                                           | Documenta las extensiones de nombre de archivo de metarchivo con reglas e instrucciones sobre su uso.                                                  |



 

Windows Los metarchivos multimedia son archivos de texto que proporcionan información sobre una secuencia de archivos y su presentación. Los metarchivos se basan en la sintaxis lenguaje de marcado extensible (XML) y se basan en varios elementos de tipo XML con sus etiquetas y atributos. Cada elemento define una configuración o una acción para los medios de streaming.

Hay dos conjuntos de etiquetas de elemento disponibles para los metarchivos. Los metarchivos del lado cliente tienen un conjunto de elementos y los metarchivos del lado servidor tienen otro conjunto de elementos.

Si una etiqueta de elemento no tiene ningún elemento secundario (los que modifican o están contenidos dentro de otro elemento), se puede usar un carácter de barra diagonal única (/) al final de la etiqueta de apertura en lugar de una etiqueta de cierre. Si los elementos secundarios no aparecen entre la etiqueta de apertura y cierre de un elemento, no son elementos secundarios para ese elemento y se omiten o provocan un error en la sintaxis del metarchivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca Windows metarchivos multimedia**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Metarchivos multimedia**](windows-media-metafiles.md)
</dt> </dl>

 

 




