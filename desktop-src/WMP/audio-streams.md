---
title: Secuencias de audio
description: Secuencias de audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player tiendas en línea, secuencias de audio
- tiendas en línea, secuencias de audio
- tipo 1 almacenes en línea, secuencias de audio
- Windows Media Player tiendas en línea, secuencias de servidores de música
- tiendas en línea, secuencias de servidores de música
- tipo 1 tiendas en línea, secuencias de servidores de música
- Windows Media Player tiendas en línea, secuencias del servidor de música
- tiendas en línea, secuencias del servidor de música
- tipo 1 almacenes en línea, secuencias del servidor de música
- secuencias de audio
- secuencias del servidor de música
- flujos de servidores de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077341"
---
# <a name="audio-streams"></a><span data-ttu-id="625e0-115">Secuencias de audio</span><span class="sxs-lookup"><span data-stu-id="625e0-115">Audio Streams</span></span>

<span data-ttu-id="625e0-116">Las tiendas en línea pueden proporcionar música como una transmisión desde un servidor de música.</span><span class="sxs-lookup"><span data-stu-id="625e0-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="625e0-117">Esto resulta útil para proporcionar ejemplos, elementos promocionales especiales o para permitir que los usuarios de la suscripción disfruten de música sin tener que descargar el contenido.</span><span class="sxs-lookup"><span data-stu-id="625e0-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="625e0-118">No es habitual almacenar la dirección URL de la secuencia como parte del catálogo de música, sino que debe resolver la dirección URL justo antes de la reproducción basada en el identificador de pista.</span><span class="sxs-lookup"><span data-stu-id="625e0-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="625e0-119">Para habilitar esto, Windows Media Player llama a [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) y proporciona el tipo de transmisión por secuencias (como un valor de enumeración [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) y el identificador de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="625e0-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="625e0-120">El complemento devuelve la dirección URL del flujo a través del parámetro *pbstrURL* .</span><span class="sxs-lookup"><span data-stu-id="625e0-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="625e0-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="625e0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="625e0-122">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="625e0-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




