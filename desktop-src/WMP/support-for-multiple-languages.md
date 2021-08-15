---
title: Compatibilidad con varios idiomas
description: Compatibilidad con varios idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Listas de reproducción de metarchivo multimedia, compatibilidad con varios idiomas
- listas de reproducción de metarchivo, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Windows Listas de reproducción de metarchivo multimedia, compatibilidad con varios idiomas
- listas de reproducción de metarchivo, compatibilidad con varios idiomas
- listas de reproducción, compatibilidad con varios idiomas
- Windows Listas de reproducción de metarchivo multimedia, compatibilidad con idiomas
- listas de reproducción de metarchivo, compatibilidad con idiomas
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002075"
---
# <a name="support-for-multiple-languages"></a>Compatibilidad con varios idiomas

Reproductor de Windows Media serie 9 o posterior admite metadatos Windows multimedia creados mediante el juego de caracteres Unicode. Esto le permite incluir metadatos multilingües en la lista de reproducción de metarchivo. Las reglas siguientes rigen el uso de metadatos multilingües en Windows metarchivos multimedia:

-   Los caracteres se deben codificar mediante el esquema de codificación UTF-8.
-   La lista de reproducción de metarchivo debe incluir el **siguiente PARÁMETRO en** el nivel de lista de reproducción:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Solo Reproductor de Windows Media serie 9 o posterior admite esta funcionalidad.
-   Si la lista de reproducción de metarchivo no se guarda con codificación UTF-8 y el elemento **PARAM** correcto, se analizará mediante la página de códigos de configuración regional del sistema predeterminada del equipo del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Windows Introducción a los metarchivos multimedia**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




