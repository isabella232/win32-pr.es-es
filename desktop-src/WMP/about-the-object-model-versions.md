---
title: Acerca de las versiones del modelo de objetos
description: Acerca de las versiones del modelo de objetos
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versiones
- Modelo de objetos de Windows Media Player, versiones
- modelo de objetos, versiones
- Control ActiveX de Windows Media Player, versiones para el modelo de objetos
- Control ActiveX, versiones para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, versiones para el modelo de objetos
- Windows Media Player Mobile, versiones para el modelo de objetos
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420440"
---
# <a name="about-the-object-model-versions"></a>Acerca de las versiones del modelo de objetos

Windows Media Player 7,0 presentó un nuevo modelo de objetos. Este modelo de objetos se ha ampliado con Windows Media Player 7,1, Windows Media Player para Windows XP, Windows Media Player series 9, Windows Media Player 10, Windows Media Player 11 y Windows Media Player 12. Cada tema de la referencia del modelo de objetos incluye una sección de requisitos que detalla el requisito mínimo para la propiedad, el método o el evento individual. En las siguientes listas se detallan los nuevos objetos, métodos, propiedades y eventos que se han agregado para cada versión desde la versión 7,0. Estas listas también incluyen nuevas interfaces, métodos y eventos de C++.

Cuando una interfaz nueva o actualizada también se expone como un objeto, solo se muestra el objeto. Para buscar la interfaz, consulte la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md). Normalmente, simplemente necesitará agregar el prefijo IWMP al nombre del objeto. Si una nueva interfaz extiende una existente, puede que tenga que buscar el número de versión más reciente. Por ejemplo, Windows Media Player 9 series presentaron nuevas propiedades y métodos disponibles en el objeto de [**configuración**](settings-object.md) . En C++, están disponibles a través de la interfaz [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , que extiende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Agregado para Windows Media Player 7,1

-   [**Player. stretchToFit (propiedad)**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Agregado para Windows Media Player para Windows XP

-   [**Controls. Step (método)**](controls-step.md)
-   [**Objeto de DVD**](dvd-object.md)
-   [**Media. error (propiedad)**](media-error.md)
-   [**Evento Player. DomainChange**](player-player-domainchange.md)
-   [**Evento Player. MediaError**](player-player-mediaerror.md)
-   [**Evento Player. OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Player. windowlessVideo (propiedad)**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Agregado para Windows Media Player serie 9

-   [**ClosedCaption. getSAMILangID, método**](closedcaption-getsamilangid.md)
-   [**ClosedCaption. getSAMILangName, método**](closedcaption-getsamilangname.md)
-   [**ClosedCaption. getSAMIStyleName, método**](closedcaption-getsamistylename.md)
-   [**Propiedad ClosedCaption. SAMILangCount**](closedcaption-samilangcount.md)
-   [**Propiedad ClosedCaption. SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Propiedad Controls. audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Propiedad Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Propiedad Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Propiedad Controls. currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Controls. getAudioLanguageDescription (método)**](controls-getaudiolanguagedescription.md)
-   [**Controls. getAudioLanguageID (método)**](controls-getaudiolanguageid.md)
-   [**Controls. getLanguageName (método)**](controls-getlanguagename.md)
-   [**ErrorItem. Condition (propiedad)**](erroritem-condition.md)
-   [**External. appColorLight (propiedad)**](external-appcolorlight.md)
-   [**Evento external. OnColorChange**](external-oncolorchange-event.md)
-   [**External. version (propiedad)**](external-version.md)
-   [**IWMPEvents::P evento layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents::P evento layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents:: SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents:: SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Interfaz IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Interfaz IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Interfaz IWMPSkinManager**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Método media. getAttributeCountByType**](media-getattributecountbytype.md)
-   [**Método media. getItemInfoByType**](media-getiteminfobytype.md)
-   [**Objeto MetadataPicture**](metadatapicture-object.md)
-   [**Objeto MetadataText**](metadatatext-object.md)
-   [**Evento Player. AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Player. isRemote (propiedad)**](player-isremote.md)
-   [**Evento Player. MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Player. newMedia (método)**](player-newmedia.md)
-   [**Player. reproducción (método)**](player-newplaylist.md)
-   [**Player. openPlayer (método)**](player-openplayer.md)
-   [**Player. playerApplication (propiedad)**](player-playerapplication.md)
-   [**Evento Player. StatusChange**](player-player-statuschange.md)
-   [**Objeto PlayerApplication**](playerapplication-object.md)
-   [**Propiedad settings. defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**Propiedad settings. mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Settings. requestMediaAccessRights (método)**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Agregado para Windows Media Player 10

-   [**Interfaz IWMPGraphCreation**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**Interfaz IWMPPlayerServices2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Interfaz IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Interfaz IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Enumeración WMPDeviceStatus**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Enumeración WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Agregado para Windows Media Player 11

-   [**Interfaz IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
-   [**Interfaz IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interfaz IWMPCdromRip (VB y C#)**](iwmpcdromrip--vb-and-c.md)
-   [**Interfaz IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Interfaz IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interfaz IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
-   [**Interfaz IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
-   [**Interfaz IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interfaz IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interfaz IWMPMediaCollection2 (VB y C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Interfaz IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
-   [**Interfaz IWMPRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**Interfaz IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interfaz IWMPStringCollection2 (VB y C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**Interfaz IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interfaz IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Query (objeto)**](query-object.md)
-   [**Enumeración WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Enumeración WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Enumeración WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Enumeración WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Agregado para Windows Media Player 12

-   [**Interfaz IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**Interfaz IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**Interfaz IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**Interfaz IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




