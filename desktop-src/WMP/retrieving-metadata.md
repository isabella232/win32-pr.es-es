---
title: Recuperación de metadatos
description: Recuperación de metadatos
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Listas de reproducción de metarchivo multimedia, recuperación de metadatos
- listas de reproducción, recuperar metadatos
- listas de reproducción de metarchivo, recuperar metadatos
- Windows Listas de reproducción de metarchivos multimedia, recuperación de metadatos
- listas de reproducción, recuperación de metadatos
- listas de reproducción de metarchivo, recuperación de metadatos
- metadata,retrieving
- recuperar metadatos
- Reproductor de Windows Media, recuperar metadatos
- Reproductor de Windows Media,recuperación de metadatos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aad75f6d35108a21b772c58d0b7a0fed9b22b5247f829988ec6e9403e0fec561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833632"
---
# <a name="retrieving-metadata"></a>Recuperación de metadatos

Mientras se reproduce un clip o una presentación, el script puede recuperar metadatos, como title y author, mediante los métodos **getItemInfo** de los objetos Reproductor de Windows Media **Media** y **Playlist.** Puede recuperar metadatos del ámbito ASX mediante métodos de objeto **De** lista de reproducción y desde el ámbito ENTRY mediante **métodos de objeto** Multimedia.

Por ejemplo, para recuperar los valores de AUTHOR, ABSTRACT y PARAM en el archivo siguiente, use el método **getItemInfo** del objeto **Playlist.** El nombre del atributo es necesario para este método. Los nombres de atributo se pueden obtener proporcionando el número de índice a la **propiedad attributeName.** Los índices disponibles para un objeto **Playlist** se pueden obtener mediante la **propiedad attributeCount.**

## <a name="example-code"></a>Código de ejemplo


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



Para recuperar los valores del objeto **Multimedia** actual en el ámbito ENTRY para REF, TITLE, COPYRIGHT y PARAM ("tres"), use la propiedad **currentMedia** del **objeto Player.** Use la **propiedad attributeCount** del **objeto Media** para determinar el número de atributos disponibles para el objeto **Media** especificado. Use números de índice con **el método getItemInfoByAtom para** recuperar valores de atributo. Use números de índice con el **método getAttributeName** del objeto **Media** para determinar los nombres de los atributos disponibles y, a continuación, use los resultados con el **método getItemInfo.**

Para obtener un ejemplo del uso de Reproductor de Windows Media de objetos para recuperar metadatos, vea [Playlist.attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




