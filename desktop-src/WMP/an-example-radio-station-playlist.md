---
title: Lista de reproducción de una estación de radio de ejemplo
description: Lista de reproducción de una estación de radio de ejemplo
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Listas de reproducción de metarchivo multimedia, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivo, ejemplos de listas de reproducción
- Windows Listas de reproducción de metarchivo multimedia, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivo, listas de reproducción de ejemplo
- Windows Listas de reproducción de metarchivo multimedia, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivo, listas de reproducción de ejemplo
- Windows Listas de reproducción de metarchivo multimedia, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivo, ejemplo de código
- Windows Lista de reproducción de metarchivo multimedia, ejemplo de lista de reproducción de estación de radio
- lista de reproducción, ejemplo de lista de reproducción de estación de radio
- ejemplo de listas de reproducción de metarchivo, lista de reproducción de estación de radio
- Reproductor de Windows Media,ejemplos de lista de reproducción
- Reproductor de Windows Media,listas de reproducción de ejemplo
- Reproductor de Windows Media,listas de reproducción de ejemplo
- Reproductor de Windows Media,ejemplo de lista de reproducción de estación de radio
- ejemplos de lista de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6db52d8eb9f109df870e65f79906761cfadee4a7871f4776fae3122dd93c8605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055033"
---
# <a name="an-example-radio-station-playlist"></a>Lista de reproducción de una estación de radio de ejemplo

En el código de ejemplo siguiente se muestra cómo crear una lista de reproducción para examinar tres estaciones de radio de roca. La empresa ficticia Adventure Works Radio está en la lista de reproducción y en todas las secuencias individuales dentro de la lista de reproducción. Al escribir el código, cambie todas las direcciones URL y nombres de archivo por nombres de archivo válidos que sean accesibles para su Reproductor de Windows Media.

Se crea una lista de reproducción para cada una de las estaciones. Una cuarta lista de reproducción examina las tres primeras. Las listas de reproducción se crean para hacer referencia a anuncios generados dinámicamente y tienen personal de marca de Adventure Works Radio.

Una de las listas de reproducción que representa una estación de radio podría tener este aspecto.


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



La lista de reproducción se puede construir a partir de referencias a las listas de reproducción individuales.

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



En este ejemplo se reproduciría un anuncio seguido de 30 segundos de cada una de las tres estaciones a las que se hace referencia, una después de la otra. Este ciclo se repetirá indefinidamente porque no se ha definido el atributo **COUNT** del elemento **REPEAT.**

-   Las empresas, las organizaciones, los productos, las personas y los eventos usados en los ejemplos son ficticios. No se entenderá o deducirá ninguna asociación con ninguna empresa, organización, producto, persona o acontecimiento reales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




