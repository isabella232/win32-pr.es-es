---
title: Acerca de las versiones del modelo de objetos
description: Acerca de las versiones del modelo de objetos
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Reproductor de Windows Media,versions
- Reproductor de Windows Media modelo de objetos, versiones
- modelo de objetos, versiones
- Reproductor de Windows Media ActiveX control,versions para el modelo de objetos
- ActiveX control,versiones para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,versiones para el modelo de objetos
- Reproductor de Windows Media Mobile,versions para el modelo de objetos
- versiones de Reproductor de Windows Media,object model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce90455d93d71f6fde62b97d3b4d38e34963307e60b831c8110a914cc535cffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510065"
---
# <a name="about-the-object-model-versions"></a>Acerca de las versiones del modelo de objetos

Reproductor de Windows Media 7.0 introdujo un nuevo modelo de objetos. Este modelo de objetos se ha ampliado con Reproductor de Windows Media 7.1, Reproductor de Windows Media para Windows XP, Reproductor de Windows Media serie 9, Reproductor de Windows Media 10, Reproductor de Windows Media 11 y Reproductor de Windows Media 12. Cada tema de la Referencia del modelo de objetos incluye una sección Requisitos que detalla el requisito mínimo para la propiedad, el método o el evento individuales. En las listas siguientes se detallan los nuevos objetos, métodos, propiedades y eventos que se han agregado para cada versión desde la versión 7.0. Estas listas también incluyen nuevas interfaces, métodos y eventos de C++.

Cuando una interfaz nueva o actualizada también se expone como un objeto, solo se muestra el objeto . Para buscar la interfaz, consulte referencia del modelo [de objetos para C++.](object-model-reference-for-c.md) Normalmente, basta con agregar el prefijo IWMP al nombre del objeto. Si una nueva interfaz extiende una existente, es posible que tenga que buscar el número de versión más reciente. Por ejemplo, Reproductor de Windows Media serie 9 introdujo nuevas propiedades y métodos disponibles en [**el Configuración**](settings-object.md) objeto . En C++, están disponibles a través de la [**interfaz IWMPSettings2,**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) que extiende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Se ha agregado para Reproductor de Windows Media 7.1

-   [**Player.stretchToFit (Propiedad)**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Se ha agregado Reproductor de Windows Media para Windows XP

-   [**Controls.step (método)**](controls-step.md)
-   [**Objeto DVD**](dvd-object.md)
-   [**Media.error (Propiedad)**](media-error.md)
-   [**Evento Player.DomainChange**](player-player-domainchange.md)
-   [**Evento Player.MediaError**](player-player-mediaerror.md)
-   [**Evento Player.OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Player.windowlessVideo (Propiedad)**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Se ha agregado para Reproductor de Windows Media serie 9

-   [**Método ClosedCaption.getSAMILangID**](closedcaption-getsamilangid.md)
-   [**Método ClosedCaption.getSAMILangName**](closedcaption-getsamilangname.md)
-   [**Método ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
-   [**Propiedad ClosedCaption.SAMILangCount**](closedcaption-samilangcount.md)
-   [**Propiedad ClosedCaption.SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Propiedad Controls.audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Propiedad Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Propiedad Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Propiedad Controls.currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Controls.getAudioLanguageDescription (método)**](controls-getaudiolanguagedescription.md)
-   [**Controls.getAudioLanguageID (método)**](controls-getaudiolanguageid.md)
-   [**Controls.getLanguageName (método)**](controls-getlanguagename.md)
-   [**ErrorItem.condition (Propiedad)**](erroritem-condition.md)
-   [**Propiedad External.appColorLight**](external-appcolorlight.md)
-   [**Evento External.OnColorChange**](external-oncolorchange-event.md)
-   [**Propiedad External.version**](external-version.md)
-   [**Evento IWMPEvents::P layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**Evento IWMPEvents::P layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents::SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents::SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**IWMPPlayerServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**IWMPRemoteMediaServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**IWMPSkinManager (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Media.getAttributeCountByType (método)**](media-getattributecountbytype.md)
-   [**Media.getItemInfoByType (método)**](media-getiteminfobytype.md)
-   [**MetadataPicture (objeto)**](metadatapicture-object.md)
-   [**MetadataText (objeto)**](metadatatext-object.md)
-   [**Evento Player.AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Player.isRemote (Propiedad)**](player-isremote.md)
-   [**Evento Player.MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Player.newMedia (método)**](player-newmedia.md)
-   [**Player.newPlaylist (método)**](player-newplaylist.md)
-   [**Player.openPlayer (método)**](player-openplayer.md)
-   [**Player.playerApplication (propiedad)**](player-playerapplication.md)
-   [**Evento Player.StatusChange**](player-player-statuschange.md)
-   [**Objeto PlayerApplication**](playerapplication-object.md)
-   [**Configuración.defaultAudioLanguage (Propiedad)**](settings-defaultaudiolanguage.md)
-   [**Configuración.mediaAccessRights (Propiedad)**](settings-mediaaccessrights.md)
-   [**Configuración.requestMediaAccessRights (Método)**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Se ha agregado para Reproductor de Windows Media 10

-   [**IWMPGraphCreation (interfaz)**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**IWMPPlayerServices2 (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**IWMPSyncDevice (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**IWMPSyncServices (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**WMPDeviceStatus (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**WMPSyncState (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Se ha agregado para Reproductor de Windows Media 11

-   [**IWMPCdromRom Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
-   [**IWMPCdromRip (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interfaz IWMPCdromRip (VB y C#)**](iwmpcdromrip--vb-and-c.md)
-   [**IWMPEvents3 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**IWMPFolderMonitorServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPLibrary (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
-   [**IWMPLibraryServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
-   [**IWMPLibrarySharingServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interfaz IWMPMediaCollection2 (VB y C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**IWMPQuery (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
-   [**IWMPRenderConfig (interfaz)**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**IWMPStringCollection2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interfaz IWMPStringCollection2 (VB y C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**IWMPSyncDevice2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig (interfaz)**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Objeto Query**](query-object.md)
-   [**WMPFormat (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**WMPLevelState (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**WMPLibraryType (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**WMPRipState (enumeración)**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Se ha agregado para Reproductor de Windows Media 12

-   [**IWMPAudioRenderConfig (interfaz)**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




