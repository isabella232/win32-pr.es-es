---
description: Información general del sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Información general del sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536592"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="2e8da-103">Información general del sistema DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e8da-103">DirectShow System Overview</span></span>

<span data-ttu-id="2e8da-104">**El reto de los elementos multimedia**</span><span class="sxs-lookup"><span data-stu-id="2e8da-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="2e8da-105">Trabajar con multimedia presenta varios desafíos principales:</span><span class="sxs-lookup"><span data-stu-id="2e8da-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="2e8da-106">Las secuencias multimedia contienen grandes cantidades de datos, que se deben procesar muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2e8da-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="2e8da-107">El audio y el vídeo deben estar sincronizados para que se inicie y se detenga al mismo tiempo y se reproduzcan a la misma velocidad.</span><span class="sxs-lookup"><span data-stu-id="2e8da-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="2e8da-108">Los datos pueden provienen de varios orígenes, como archivos locales, redes de equipos, difusiones de televisión y cámaras de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e8da-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="2e8da-109">Los datos tienen una variedad de formatos, como Audio-Video intercalados (AVI), el formato de streaming avanzado (ASF), el grupo de expertos en imágenes de movimiento (MPEG) y vídeo digital (DV).</span><span class="sxs-lookup"><span data-stu-id="2e8da-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="2e8da-110">El programador no sabe de antemano qué dispositivos de hardware estarán presentes en el sistema del usuario final.</span><span class="sxs-lookup"><span data-stu-id="2e8da-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="2e8da-111">**La solución de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="2e8da-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="2e8da-112">DirectShow está diseñado para abordar cada uno de estos desafíos.</span><span class="sxs-lookup"><span data-stu-id="2e8da-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="2e8da-113">Su objetivo de diseño principal es simplificar la tarea de crear aplicaciones multimedia digitales en la plataforma Windows, aislando las aplicaciones de las complejidades de los transportes de datos, las diferencias de hardware y la sincronización.</span><span class="sxs-lookup"><span data-stu-id="2e8da-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="2e8da-114">Para lograr el rendimiento necesario para transmitir vídeo y audio, DirectShow usa Direct3D y DirectSound siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="2e8da-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="2e8da-115">Estas tecnologías representan los datos de forma eficaz en las tarjetas de sonido y gráficos del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e8da-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="2e8da-116">DirectShow sincroniza la reproducción encapsulando los datos multimedia en muestras con marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2e8da-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="2e8da-117">Para controlar la variedad de orígenes, formatos y dispositivos de hardware que son posibles, DirectShow utiliza una arquitectura modular, en la que la aplicación se mezcla y coincide con los distintos componentes de software denominados *filtros*.</span><span class="sxs-lookup"><span data-stu-id="2e8da-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="2e8da-118">DirectShow proporciona filtros que admiten dispositivos de captura y optimización basados en el Modelo de controlador de Windows (WDM), así como filtros que admiten tarjetas de captura antiguas de vídeo para Windows (VfW) y códecs escritos para las interfaces del administrador de compresión de audio (ACM) y el administrador de compresión de vídeo (VCM).</span><span class="sxs-lookup"><span data-stu-id="2e8da-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="2e8da-119">En el diagrama siguiente se muestra la relación entre una aplicación, los componentes de DirectShow y algunos de los componentes de hardware y software compatibles con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2e8da-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![arquitectura de alto nivel](images/arch-oview2.png)

<span data-ttu-id="2e8da-121">Como se muestra aquí, los filtros de DirectShow se comunican con y controlan una amplia variedad de dispositivos, como el sistema de archivos local, tarjetas de captura de vídeo y sintonizador de TV, códecs VfW, la pantalla de vídeo (a través de DirectDraw o GDI) y la tarjeta de sonido (a través de DirectSound).</span><span class="sxs-lookup"><span data-stu-id="2e8da-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="2e8da-122">Por lo tanto, DirectShow aísla la aplicación de muchas de las complejidades de estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2e8da-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="2e8da-123">DirectShow también proporciona filtros de compresión y descompresión nativos para determinados formatos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2e8da-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e8da-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e8da-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e8da-125">Acerca de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e8da-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



