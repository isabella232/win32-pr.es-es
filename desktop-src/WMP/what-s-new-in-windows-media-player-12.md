---
title: Novedades del Reproductor de Windows Media 12
description: En este tema se enumeran las características nuevas de Windows Media Player 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, novedades
- Windows Media Player, nuevas características
- Kit de desarrollo de software (SDK), Windows Media Player 12
- SDK (kit de desarrollo de software), Windows Media Player 12
- documentación, SDK de Windows Media Player 12
- novedades, Windows Media Player 12
- nuevas características, Windows Media Player 12
- interfaces, nuevas características de Windows Media Player 12
- atributos, nuevas características de Windows Media Player 12
- metadatos, nuevas características de Windows Media Player 12
- enumeraciones, nuevas características de Windows Media Player 12
- marcas, nuevas características de Windows Media Player 12
- interfaces, desusadas en Windows Media Player 12
- métodos, desusados en Windows Media Player 11 y no 12
- versiones de Windows Media Player, nuevas características de la versión 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104149139"
---
# <a name="whats-new-in-windows-media-player-12"></a>Novedades del Reproductor de Windows Media 12

En este tema se enumeran las características nuevas de Windows Media Player 12.

## <a name="new-interfaces"></a>Nuevas interfaces

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Nuevos atributos

Los siguientes atributos nuevos para los elementos multimedia están disponibles a través de las interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) y [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**IdBiblioteca**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Nuevos metadatos de dispositivo

Los siguientes elementos de metadatos de dispositivo nuevos se pueden recuperar llamando a [**IWMPSyncDevice:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

Los siguientes elementos de metadatos de dispositivo nuevos se pueden establecer mediante una llamada a [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Nuevo miembro de enumeración

La enumeración [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) tiene el siguiente miembro nuevo.

-   **wmpssEstimating**

## <a name="new-flag"></a>Nueva marca

El método [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) admite la siguiente marca nueva.

-   **marcas de WMPGC \_ \_ usar \_ \_ gráfico personalizado**

## <a name="deprecated-interface"></a>Interfaz desusada

La interfaz siguiente está en desuso.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Métodos que ya no están en desuso

Los siguientes métodos estaban en desuso en el SDK de Windows Media Player 11, pero ya no están en desuso.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del SDK de Windows Media Player](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




