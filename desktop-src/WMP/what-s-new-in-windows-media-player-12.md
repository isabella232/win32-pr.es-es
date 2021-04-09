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
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="a853c-118">Novedades del Reproductor de Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="a853c-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="a853c-119">En este tema se enumeran las características nuevas de Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="a853c-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="a853c-120">Nuevas interfaces</span><span class="sxs-lookup"><span data-stu-id="a853c-120">New Interfaces</span></span>

-   [<span data-ttu-id="a853c-121">**IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="a853c-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="a853c-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="a853c-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="a853c-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="a853c-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="a853c-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="a853c-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="a853c-125">Nuevos atributos</span><span class="sxs-lookup"><span data-stu-id="a853c-125">New Attributes</span></span>

<span data-ttu-id="a853c-126">Los siguientes atributos nuevos para los elementos multimedia están disponibles a través de las interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) y [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .</span><span class="sxs-lookup"><span data-stu-id="a853c-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="a853c-127">**AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="a853c-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="a853c-128">**AlternateSourceURL**</span><span class="sxs-lookup"><span data-stu-id="a853c-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="a853c-129">**DLNASourceURI**</span><span class="sxs-lookup"><span data-stu-id="a853c-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="a853c-130">**DLNAServerUDN**</span><span class="sxs-lookup"><span data-stu-id="a853c-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="a853c-131">**DTCPIPHost**</span><span class="sxs-lookup"><span data-stu-id="a853c-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="a853c-132">**DTCPIPPort**</span><span class="sxs-lookup"><span data-stu-id="a853c-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="a853c-133">**IdBiblioteca**</span><span class="sxs-lookup"><span data-stu-id="a853c-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="a853c-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="a853c-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="a853c-135">Nuevos metadatos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a853c-135">New Device Metadata</span></span>

<span data-ttu-id="a853c-136">Los siguientes elementos de metadatos de dispositivo nuevos se pueden recuperar llamando a [**IWMPSyncDevice:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="a853c-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="a853c-137">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="a853c-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="a853c-138">**SkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="a853c-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="a853c-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="a853c-139">**SyncFilter**</span></span>

<span data-ttu-id="a853c-140">Los siguientes elementos de metadatos de dispositivo nuevos se pueden establecer mediante una llamada a [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span><span class="sxs-lookup"><span data-stu-id="a853c-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="a853c-141">**AutoSyncDefaultRules**</span><span class="sxs-lookup"><span data-stu-id="a853c-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="a853c-142">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="a853c-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="a853c-143">**IncludeSkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="a853c-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="a853c-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="a853c-144">**SyncFilter**</span></span>
-   <span data-ttu-id="a853c-145">**SyncOnConnect**</span><span class="sxs-lookup"><span data-stu-id="a853c-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="a853c-146">Nuevo miembro de enumeración</span><span class="sxs-lookup"><span data-stu-id="a853c-146">New Enumeration Member</span></span>

<span data-ttu-id="a853c-147">La enumeración [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) tiene el siguiente miembro nuevo.</span><span class="sxs-lookup"><span data-stu-id="a853c-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="a853c-148">**wmpssEstimating**</span><span class="sxs-lookup"><span data-stu-id="a853c-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="a853c-149">Nueva marca</span><span class="sxs-lookup"><span data-stu-id="a853c-149">New Flag</span></span>

<span data-ttu-id="a853c-150">El método [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) admite la siguiente marca nueva.</span><span class="sxs-lookup"><span data-stu-id="a853c-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="a853c-151">**marcas de WMPGC \_ \_ usar \_ \_ gráfico personalizado**</span><span class="sxs-lookup"><span data-stu-id="a853c-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="a853c-152">Interfaz desusada</span><span class="sxs-lookup"><span data-stu-id="a853c-152">Deprecated Interface</span></span>

<span data-ttu-id="a853c-153">La interfaz siguiente está en desuso.</span><span class="sxs-lookup"><span data-stu-id="a853c-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="a853c-154">**IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="a853c-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="a853c-155">Métodos que ya no están en desuso</span><span class="sxs-lookup"><span data-stu-id="a853c-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="a853c-156">Los siguientes métodos estaban en desuso en el SDK de Windows Media Player 11, pero ya no están en desuso.</span><span class="sxs-lookup"><span data-stu-id="a853c-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="a853c-157">**IWMPGraphCreation::GraphCreationPreRender**</span><span class="sxs-lookup"><span data-stu-id="a853c-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="a853c-158">**IWMPGraphCreation::GraphCreationPostRender**</span><span class="sxs-lookup"><span data-stu-id="a853c-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="a853c-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a853c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a853c-160">Acerca del SDK de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="a853c-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




