---
title: Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2
description: Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Reproductor de Windows Media en línea, ejemplo de documento ServiceInfo
- tiendas en línea, ejemplo de documento ServiceInfo
- tiendas en línea de tipo 2, ejemplo de documento ServiceInfo
- Reproductor de Windows Media tiendas en línea,documento ServiceInfo
- tiendas en línea,documento ServiceInfo
- tiendas en línea de tipo 2, documento ServiceInfo
- Reproductor de Windows Media en línea, ejemplo de código
- tiendas en línea, ejemplo de código
- tiendas en línea de tipo 2, ejemplo de código
- Documento ServiceInfo de ejemplo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7962f7548f8c880e60320d3a7fb071e2a076ffafdac9a56b4cf6d8aa41b5d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650125"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a>Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2

En el ejemplo de código siguiente se muestra un ServiceInfo.xml completo. Puede usar este XML como punto de partida para su propio documento ServiceInfo.


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware">
    <FriendlyName>Proseware Service</FriendlyName>
    <Image 
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/30x30.jpg" />
    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>
    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>
    <ServiceTask2
        URL = "https://www.proseware.com/service/html/Video.asp">
        <ButtonText>Proseware\nVideo</ButtonText>
        <ButtonTip>Proseware Video</ButtonTip>
    </ServiceTask2>
    <ServiceTask3
        URL = "https://www.proseware.com/service/html/Radio.asp">
        <ButtonText>Proseware\nRadio</ButtonText>
        <ButtonTip>Proseware Radio</ButtonTip>
    </ServiceTask3>
    <Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
    </Navigate>
    <InfoCenter
        URL = "https://www.proseware.com/service/html/InfoCenter.asp"/>
    <AlbumInfo
        URL = "https://www.proseware.com/service/html/AlbumInfo.asp"/>
    <BuyCD
        MediaPlayerURL = "https://www.proseware.com/service/html/BuyCDMediaPlayer.asp"
        MediaCenterURL = "https://www.proseware.com/service/html/BuyCDMediaCenter.asp"
        BrowserURL = "https://www.proseware.com/service/html/BuyCDBrowser.asp"/>
    <DownloadStatus
        URL = "https://www.proseware.com/service/html/Music_Download.htm"/>
    <HTMLView
        BaseURL = "https://www.proseware.com/"/>
</ServiceInfo>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




