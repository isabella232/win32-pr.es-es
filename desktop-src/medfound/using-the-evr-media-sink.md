---
description: Uso del receptor de medios de EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del receptor de medios de EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717396"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="e5eb3-103">Uso del receptor de medios de EVR</span><span class="sxs-lookup"><span data-stu-id="e5eb3-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="e5eb3-104">El receptor de medios de representador de vídeo mejorado (EVR) se puede usar como un componente independiente.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="e5eb3-105">Sin embargo, a menudo, una aplicación creará el receptor de medios EVR dentro de una topología y, a continuación, usará la sesión multimedia para controlar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="e5eb3-106">Hay dos maneras de crear el receptor de medios EVR:</span><span class="sxs-lookup"><span data-stu-id="e5eb3-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="e5eb3-107">La función [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="e5eb3-108">La función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un objeto de activación para el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="e5eb3-109">El receptor de medios EVR inicialmente tiene un receptor de flujo, que corresponde al flujo de referencia.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="e5eb3-110">Para agregar nuevos receptores de secuencia, llame a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="e5eb3-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5eb3-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5eb3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5eb3-112">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="e5eb3-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="e5eb3-113">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="e5eb3-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



