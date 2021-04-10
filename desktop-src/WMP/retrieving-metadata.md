---
title: Recuperación de metadatos
description: Recuperación de metadatos
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Listas de reproducción de metarchivos de Windows Media, recuperar metadatos
- listas de reproducción, recuperar metadatos
- listas de reproducción de metarchivos, recuperar metadatos
- Listas de reproducción de metarchivos de Windows Media, recuperación de metadatos
- listas de reproducción, recuperación de metadatos
- listas de reproducción de metarchivos, recuperación de metadatos
- metadatos, recuperar
- recuperar metadatos
- Windows Media Player, recuperar metadatos
- Windows Media Player, recuperación de metadatos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994368"
---
# <a name="retrieving-metadata"></a>Recuperación de metadatos

Mientras se reproduce un programa o un clip, el script puede recuperar metadatos, como el título y el autor, mediante los métodos **getItemInfo** de los objetos **multimedia** y **lista de reproducción** de Windows Media Player. Puede recuperar los metadatos del ámbito de ASX mediante métodos de objeto de **lista de reproducción** y desde el ámbito de entrada mediante métodos de objetos **multimedia** .

Por ejemplo, para recuperar los valores de AUTHOR, ABSTRACT y PARAM en el siguiente archivo, use el método **getItemInfo** del objeto de **lista de reproducción** . El nombre de atributo es necesario para este método. Los nombres de atributo se pueden obtener proporcionando el número de índice a la propiedad **attributeName** . Los índices disponibles para un objeto de **lista de reproducción** se pueden obtener mediante la propiedad **attributeCount** .

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



Para recuperar los valores del objeto **multimedia** actual en el ámbito de entrada para ref, title, copyright y param ("tres"), use la propiedad **CurrentMedia** del objeto **Player** . Use la propiedad **attributeCount** del objeto **multimedia** para determinar el número de atributos disponibles para el objeto **multimedia** especificado. Use los números de índice con el método **getItemInfoByAtom** para recuperar los valores de atributo. Use los números de índice con el método **getAttributeName** del objeto **multimedia** para determinar los nombres de los atributos disponibles y, a continuación, use los resultados con el método **getItemInfo** .

Para obtener un ejemplo del uso de métodos de objetos de Media Player de Windows para recuperar metadatos, vea [playlist. attributeCount](playlist-attributecount.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




