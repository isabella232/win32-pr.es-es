---
title: Novedades del Reproductor de Windows Media 12
description: En este tema se enumeran las características nuevas de Reproductor de Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Reproductor de Windows Media, novedades
- Reproductor de Windows Media,nuevas características
- kit de desarrollo de software (SDK),Reproductor de Windows Media 12
- SDK (kit de desarrollo de software),Reproductor de Windows Media 12
- documentation,Reproductor de Windows Media 12 SDK
- novedades, Reproductor de Windows Media 12
- nuevas características, Reproductor de Windows Media 12
- interfaces,nuevas características de Reproductor de Windows Media 12
- atributos, nuevas características de Reproductor de Windows Media 12
- metadata,new features in Reproductor de Windows Media 12
- enumeraciones, nuevas características de Reproductor de Windows Media 12
- flags,new features in Reproductor de Windows Media 12
- interfaces, en desuso en Reproductor de Windows Media 12
- methods, en desuso Reproductor de Windows Media 11 y no 12
- versiones de Reproductor de Windows Media,nuevas características de la versión 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243027"
---
# <a name="whats-new-in-windows-media-player-12"></a>Novedades del Reproductor de Windows Media 12

En este tema se enumeran las características nuevas de Reproductor de Windows Media 12.

## <a name="new-interfaces"></a>Nuevas interfaces

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Nuevos atributos

Los siguientes atributos nuevos para elementos multimedia están disponibles a través de las interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) [**e IWMPMedia3.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**LibraryID**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Nuevos metadatos de dispositivo

Los siguientes nuevos elementos de metadatos de dispositivo se pueden recuperar llamando a [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

Los siguientes nuevos elementos de metadatos de dispositivo se pueden establecer mediante una llamada [**a IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Nuevo miembro de enumeración

La [**enumeración WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) tiene el siguiente nuevo miembro.

-   **wmpssEstimating**

## <a name="new-flag"></a>Nueva marca

El [**método IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) admite la siguiente marca nueva.

-   **LAS MARCAS DE WMPGC \_ \_ USAN GRÁFICO \_ \_ PERSONALIZADO**

## <a name="deprecated-interface"></a>Interfaz en desuso

La siguiente interfaz está en desuso.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Métodos que ya no están en desuso

Los métodos siguientes quedaron en desuso Reproductor de Windows Media SDK 11, pero ya no están en desuso.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del SDK Reproductor de Windows Media](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




