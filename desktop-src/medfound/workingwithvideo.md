---
description: Trabajar con vídeo
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Trabajar con vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361344"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="9b234-103">Trabajar con vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="9b234-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="9b234-104">Aunque los códecs de vídeo individuales tienen sus propias peculiaridades, todos utilizan los mismos procedimientos básicos.</span><span class="sxs-lookup"><span data-stu-id="9b234-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="9b234-105">En esta sección se describe cómo codificar y descodificar vídeo con los códecs de Windows Media Video y se abordan las características concretas de cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="9b234-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="9b234-106">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="9b234-106">This section contains the following topics.</span></span>



| <span data-ttu-id="9b234-107">Tema</span><span class="sxs-lookup"><span data-stu-id="9b234-107">Topic</span></span>                                                                                                        | <span data-ttu-id="9b234-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b234-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b234-109">Elección de un códec de vídeo</span><span class="sxs-lookup"><span data-stu-id="9b234-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="9b234-110">Describe los tipos de contenido que mejor se adaptan a la compresión con cada uno de los códecs Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="9b234-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="9b234-111">Configuración de la codificación de vídeo</span><span class="sxs-lookup"><span data-stu-id="9b234-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="9b234-112">Describe cómo configurar el codificador de vídeo DMOs.</span><span class="sxs-lookup"><span data-stu-id="9b234-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="9b234-113">Configuración de la descodificación de vídeo</span><span class="sxs-lookup"><span data-stu-id="9b234-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="9b234-114">Describe cómo configurar el descodificador de vídeo DMOs.</span><span class="sxs-lookup"><span data-stu-id="9b234-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="9b234-115">Inserción de fotogramas clave forzada</span><span class="sxs-lookup"><span data-stu-id="9b234-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="9b234-116">Describe cómo solicitar que un ejemplo se codifique como un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="9b234-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="9b234-117">Codificación de vídeo entrelazada</span><span class="sxs-lookup"><span data-stu-id="9b234-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="9b234-118">Describe cómo mantener el entrelazado en flujos de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="9b234-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="9b234-119">Usar el códec de perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="9b234-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="9b234-120">Describe cómo usar el códec de perfil avanzado de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="9b234-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="9b234-121">Usar el códec de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="9b234-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="9b234-122">Describe cómo usar el códec de pantalla de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="9b234-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="9b234-123">Usar el códec de imagen de Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="9b234-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="9b234-124">Describe cómo usar el códec de imagen Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="9b234-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="9b234-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b234-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b234-126">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="9b234-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



