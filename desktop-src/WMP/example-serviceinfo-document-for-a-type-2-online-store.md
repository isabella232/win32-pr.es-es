---
title: Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2
description: Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Windows Media Player tiendas en línea, ejemplo de documento de ServiceInfo
- tiendas en línea, ejemplo de documento de ServiceInfo
- tipo 2 tiendas en línea, ejemplo de documento ServiceInfo
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Windows Media Player tiendas en línea, ejemplo de código
- tiendas en línea, ejemplo de código
- tipo 2 tiendas en línea, ejemplo de código
- ejemplo de documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02214b9d7180296fa11bb877f978c6bde85f3a4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695386"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="9ec3d-114">Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="9ec3d-114">Example ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="9ec3d-115">En el ejemplo de código siguiente se muestra un documento ServiceInfo.xml completo.</span><span class="sxs-lookup"><span data-stu-id="9ec3d-115">The following code example shows a complete ServiceInfo.xml document.</span></span> <span data-ttu-id="9ec3d-116">Puede usar este XML como punto de partida para su propio documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="9ec3d-116">You can use this XML as a starting point for your own ServiceInfo document.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9ec3d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ec3d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ec3d-118">**Guía de programación para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9ec3d-118">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9ec3d-119">**Documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9ec3d-119">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9ec3d-120">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9ec3d-120">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




