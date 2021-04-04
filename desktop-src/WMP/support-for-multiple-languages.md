---
title: Compatibilidad con varios idiomas
description: Compatibilidad con varios idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con varios idiomas
- listas de reproducción de metarchivos, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con varios idiomas
- listas de reproducción de metarchivos, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Listas de reproducción de metarchivos de Windows Media, compatibilidad con idiomas
- listas de reproducción de metarchivos, compatibilidad con idiomas
- listas de reproducción, compatibilidad con idiomas
- compatibilidad con varios idiomas
- compatibilidad con varios lenguajes
- compatibilidad con el idioma
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076203"
---
# <a name="support-for-multiple-languages"></a>Compatibilidad con varios idiomas

Windows Media Player 9 series o posterior admiten los metaarchivos de Windows Media creados con el juego de caracteres Unicode. Esto le permite incluir metadatos multilingües en la lista de reproducción de metarchivo. Las siguientes reglas rigen el uso de metadatos multilingües en los metaarchivos de Windows Media:

-   Los caracteres se deben codificar mediante el esquema de codificación UTF-8.
-   La lista de reproducción del metarchivo debe incluir el **parámetro** siguiente en el nivel de lista de reproducción:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Solo Windows Media Player 9 series o versiones posteriores admiten esta funcionalidad.
-   Si la lista de reproducción del metarchivo no se guarda con la codificación UTF-8 y el elemento **param** correcto, se analizará con la página de códigos configuración regional predeterminada del sistema del equipo del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Información general de los metaarchivos de Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




