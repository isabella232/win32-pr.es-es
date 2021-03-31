---
title: Lista de reproducción de la estación de radio de ejemplo
description: Lista de reproducción de la estación de radio de ejemplo
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Listas de reproducción de metarchivos de Windows Media, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivos, ejemplos de listas de reproducción
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivos, ejemplo de código
- Listas de reproducción de metarchivo de Windows Media, ejemplo de lista de reproducción de la estación de radio
- listas de reproducción, ejemplo de lista de reproducción de la estación de radio
- listas de reproducción de metarchivo, ejemplo de lista de reproducción de la estación de radio
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Ejemplo de Windows Media Player, lista de reproducción de la estación de radio
- ejemplos de listas de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418580"
---
# <a name="an-example-radio-station-playlist"></a>Lista de reproducción de la estación de radio de ejemplo

En el ejemplo de código siguiente se muestra cómo crear una lista de reproducción para examinar tres emisoras de radio de rock. La marca de radio de Adventure Works de la empresa ficticia está en la lista de reproducción y en todas las secuencias individuales de la lista de reproducción. Al escribir el código, cambie todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que pueda tener acceso su Media Player de Windows.

Se crea una lista de reproducción para cada una de las estaciones. Una cuarta lista de reproducción examina los tres primeros. Las listas de reproducción se crean para hacer referencia a anuncios generados dinámicamente y tienen una marca de radio de Adventure Works.

Una de las listas de reproducción que representan una emisora de radio podría tener este aspecto.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



A continuación, la lista de reproducción se puede crear a partir de referencias a las listas de reproducción individuales.

Código de ejemplo


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



En este ejemplo se reproduce un anuncio seguido de 30 segundos de cada una de las tres estaciones a las que se hace referencia, una tras otra. Este ciclo se repite indefinidamente porque no se define el atributo **Count** del elemento **REPEAT** .

-   Las empresas, las organizaciones, los productos, las personas y los eventos usados en los ejemplos son ficticios. No se entenderá o deducirá ninguna asociación con ninguna empresa, organización, producto, persona o acontecimiento reales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




