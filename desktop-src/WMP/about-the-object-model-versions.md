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
# <a name="about-the-object-model-versions"></a><span data-ttu-id="3e125-111">Acerca de las versiones del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="3e125-111">About the Object Model Versions</span></span>

<span data-ttu-id="3e125-112">Windows Media Player 7,0 presentó un nuevo modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="3e125-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="3e125-113">Este modelo de objetos se ha ampliado con Windows Media Player 7,1, Windows Media Player para Windows XP, Windows Media Player series 9, Windows Media Player 10, Windows Media Player 11 y Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="3e125-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="3e125-114">Cada tema de la referencia del modelo de objetos incluye una sección de requisitos que detalla el requisito mínimo para la propiedad, el método o el evento individual.</span><span class="sxs-lookup"><span data-stu-id="3e125-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="3e125-115">En las siguientes listas se detallan los nuevos objetos, métodos, propiedades y eventos que se han agregado para cada versión desde la versión 7,0.</span><span class="sxs-lookup"><span data-stu-id="3e125-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="3e125-116">Estas listas también incluyen nuevas interfaces, métodos y eventos de C++.</span><span class="sxs-lookup"><span data-stu-id="3e125-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="3e125-117">Cuando una interfaz nueva o actualizada también se expone como un objeto, solo se muestra el objeto.</span><span class="sxs-lookup"><span data-stu-id="3e125-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="3e125-118">Para buscar la interfaz, consulte la [Referencia del modelo de objetos de C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="3e125-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="3e125-119">Normalmente, simplemente necesitará agregar el prefijo IWMP al nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="3e125-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="3e125-120">Si una nueva interfaz extiende una existente, puede que tenga que buscar el número de versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="3e125-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="3e125-121">Por ejemplo, Windows Media Player 9 series presentaron nuevas propiedades y métodos disponibles en el objeto de [**configuración**](settings-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3e125-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="3e125-122">En C++, están disponibles a través de la interfaz [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , que extiende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span><span class="sxs-lookup"><span data-stu-id="3e125-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="3e125-123">Agregado para Windows Media Player 7,1</span><span class="sxs-lookup"><span data-stu-id="3e125-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="3e125-124">**Player. stretchToFit (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="3e125-125">Agregado para Windows Media Player para Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e125-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="3e125-126">**Controls. Step (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="3e125-127">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="3e125-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="3e125-128">**Media. error (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="3e125-129">**Evento Player. DomainChange**</span><span class="sxs-lookup"><span data-stu-id="3e125-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="3e125-130">**Evento Player. MediaError**</span><span class="sxs-lookup"><span data-stu-id="3e125-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="3e125-131">**Evento Player. OpenPlaylistSwitch**</span><span class="sxs-lookup"><span data-stu-id="3e125-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="3e125-132">**Player. windowlessVideo (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="3e125-133">Agregado para Windows Media Player serie 9</span><span class="sxs-lookup"><span data-stu-id="3e125-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="3e125-134">**ClosedCaption. getSAMILangID, método**</span><span class="sxs-lookup"><span data-stu-id="3e125-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="3e125-135">**ClosedCaption. getSAMILangName, método**</span><span class="sxs-lookup"><span data-stu-id="3e125-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="3e125-136">**ClosedCaption. getSAMIStyleName, método**</span><span class="sxs-lookup"><span data-stu-id="3e125-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="3e125-137">**Propiedad ClosedCaption. SAMILangCount**</span><span class="sxs-lookup"><span data-stu-id="3e125-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="3e125-138">**Propiedad ClosedCaption. SAMIStyleCount**</span><span class="sxs-lookup"><span data-stu-id="3e125-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="3e125-139">**Propiedad Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="3e125-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="3e125-140">**Propiedad Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="3e125-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="3e125-141">**Propiedad Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="3e125-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="3e125-142">**Propiedad Controls. currentPositionTimecode**</span><span class="sxs-lookup"><span data-stu-id="3e125-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="3e125-143">**Controls. getAudioLanguageDescription (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="3e125-144">**Controls. getAudioLanguageID (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="3e125-145">**Controls. getLanguageName (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="3e125-146">**ErrorItem. Condition (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="3e125-147">**External. appColorLight (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="3e125-148">**Evento external. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="3e125-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="3e125-149">**External. version (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="3e125-150">**IWMPEvents::P evento layerDockedStateChange**</span><span class="sxs-lookup"><span data-stu-id="3e125-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="3e125-151">**IWMPEvents::P evento layerReconnect**</span><span class="sxs-lookup"><span data-stu-id="3e125-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="3e125-152">**Evento IWMPEvents:: SwitchedToControl**</span><span class="sxs-lookup"><span data-stu-id="3e125-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="3e125-153">**Evento IWMPEvents:: SwitchedToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="3e125-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="3e125-154">**Interfaz IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="3e125-155">**Interfaz IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="3e125-156">**Interfaz IWMPSkinManager**</span><span class="sxs-lookup"><span data-stu-id="3e125-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="3e125-157">**Método media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="3e125-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="3e125-158">**Método media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="3e125-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="3e125-159">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="3e125-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="3e125-160">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="3e125-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="3e125-161">**Evento Player. AudioLanguageChange**</span><span class="sxs-lookup"><span data-stu-id="3e125-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="3e125-162">**Player. isRemote (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="3e125-163">**Evento Player. MediaCollectionAttributeStringChanged**</span><span class="sxs-lookup"><span data-stu-id="3e125-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="3e125-164">**Player. newMedia (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="3e125-165">**Player. reproducción (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="3e125-166">**Player. openPlayer (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="3e125-167">**Player. playerApplication (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="3e125-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="3e125-168">**Evento Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="3e125-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="3e125-169">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="3e125-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="3e125-170">**Propiedad settings. defaultAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="3e125-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="3e125-171">**Propiedad settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3e125-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="3e125-172">**Settings. requestMediaAccessRights (método)**</span><span class="sxs-lookup"><span data-stu-id="3e125-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="3e125-173">Agregado para Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="3e125-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="3e125-174">**Interfaz IWMPGraphCreation**</span><span class="sxs-lookup"><span data-stu-id="3e125-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="3e125-175">**Interfaz IWMPPlayerServices2**</span><span class="sxs-lookup"><span data-stu-id="3e125-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="3e125-176">**Interfaz IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="3e125-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="3e125-177">**Interfaz IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="3e125-178">**Enumeración WMPDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="3e125-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="3e125-179">**Enumeración WMPSyncState**</span><span class="sxs-lookup"><span data-stu-id="3e125-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="3e125-180">Agregado para Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3e125-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="3e125-181">**Interfaz IWMPCdromBurn**</span><span class="sxs-lookup"><span data-stu-id="3e125-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="3e125-182">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="3e125-183">**Interfaz IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="3e125-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="3e125-184">**Interfaz IWMPCdromRip (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="3e125-185">**Interfaz IWMPEvents3**</span><span class="sxs-lookup"><span data-stu-id="3e125-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="3e125-186">**Interfaz IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="3e125-187">**Interfaz IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="3e125-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="3e125-188">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="3e125-189">**Interfaz IWMPLibraryServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="3e125-190">**Interfaz IWMPLibraryServices (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="3e125-191">**Interfaz IWMPLibrarySharingServices**</span><span class="sxs-lookup"><span data-stu-id="3e125-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="3e125-192">**Interfaz IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="3e125-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="3e125-193">**Interfaz IWMPMediaCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="3e125-194">**Interfaz IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="3e125-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="3e125-195">**Interfaz IWMPQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="3e125-196">**Interfaz IWMPRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="3e125-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="3e125-197">**Interfaz IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="3e125-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="3e125-198">**Interfaz IWMPStringCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e125-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="3e125-199">**Interfaz IWMPSyncDevice2**</span><span class="sxs-lookup"><span data-stu-id="3e125-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="3e125-200">**Interfaz IWMPVideoRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="3e125-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="3e125-201">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="3e125-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="3e125-202">**Enumeración WMPBurnFormat**</span><span class="sxs-lookup"><span data-stu-id="3e125-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="3e125-203">**Enumeración WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="3e125-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="3e125-204">**Enumeración WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="3e125-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="3e125-205">**Enumeración WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="3e125-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="3e125-206">Agregado para Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="3e125-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="3e125-207">**Interfaz IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="3e125-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="3e125-208">**Interfaz IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="3e125-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="3e125-209">**Interfaz IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="3e125-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="3e125-210">**Interfaz IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="3e125-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="3e125-211">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e125-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e125-212">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="3e125-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="3e125-213">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="3e125-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




