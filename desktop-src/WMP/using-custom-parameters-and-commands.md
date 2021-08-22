---
title: Uso de parámetros y comandos personalizados
description: Uso de parámetros y comandos personalizados
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Listas de reproducción de metarchivo multimedia, parámetros personalizados
- listas de reproducción, parámetros personalizados
- listas de reproducción de metarchivo, parámetros personalizados
- Windows Listas de reproducción de metarchivo multimedia, comandos personalizados
- listas de reproducción, comandos personalizados
- listas de reproducción de metarchivo, comandos personalizados
- Windows Listas de reproducción de metarchivo multimedia, parámetros
- playlists,parameters
- listas de reproducción de metarchivo, parámetros
- parámetros personalizados
- comandos personalizados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6848131c58dabfa465a202bd39b061997e2a9bbda3e8004133f1ef1ce1d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830941"
---
# <a name="using-custom-parameters-and-commands"></a>Uso de parámetros y comandos personalizados

Puede crear parámetros personalizados para pasar metadatos adicionales en una lista de reproducción de metarchivo mediante el **elemento PARAM.** Use el **atributo NAME** del elemento **PARAM** para definir el nombre del parámetro personalizado. Use el **atributo VALUE** para definir el valor del parámetro personalizado con nombre.

Recupere **los metadatos de PARAM** mediante los **métodos getItemInfo** de los **objetos Media** y **Playlist.** Para obtener un ejemplo del uso de estos métodos para recuperar metadatos, vea el [método attributeCount](playlist-attributecount.md) del objeto **Playlist.**

En la lista de reproducción de metarchivo de ejemplo siguiente se muestra el uso del **elemento PARAM** para definir parámetros personalizados.


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




