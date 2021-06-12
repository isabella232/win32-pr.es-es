---
title: Obtenga información sobre DirectShow en Windows Media Format SDK 11, una arquitectura de streaming de datos de alto nivel, modular, extensible y para la plataforma Windows.
description: Acerca de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK,DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011298"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="2dd25-107">Acerca de DirectShow (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="2dd25-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="2dd25-108">DirectShow es una arquitectura de streaming de datos modular, extensible y de alto nivel para la plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="2dd25-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="2dd25-109">Proporciona los componentes de software subyacentes y las interfaces de programación de aplicaciones (API) para una amplia variedad de aplicaciones de audio y vídeo digitales en el mercado actualmente.</span><span class="sxs-lookup"><span data-stu-id="2dd25-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="2dd25-110">DirectShow está disponible como parte del Kit de desarrollo de software de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="2dd25-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="2dd25-111">Para más información sobre DirectShow, consulte el SDK de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2dd25-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="2dd25-112">En DirectShow, todos los componentes de streaming de datos se *denominan filtros*.</span><span class="sxs-lookup"><span data-stu-id="2dd25-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="2dd25-113">Un filtro puede representar un dispositivo de hardware, un codificador o descodificador de software, un representador de audio o vídeo, o cualquier funcionalidad de procesamiento de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="2dd25-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="2dd25-114">Para permitir que las aplicaciones basadas en DirectShow lean y escriban contenido Windows Media Format, incluido el contenido protegido por Digital Rights Management (DRM), Microsoft proporciona dos filtros que encapsulan partes del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="2dd25-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="2dd25-115">Estos son el [lector de ASF de WM](wm-asf-reader-filter.md) y el escritor de [ASF de WM.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="2dd25-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="2dd25-116">Estos filtros y las interfaces que exponen se conocen colectivamente como componentes de QASF, después del archivo DLL en el que se empaquetan.</span><span class="sxs-lookup"><span data-stu-id="2dd25-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="2dd25-117">(La Q es el nombre de código inicial de DirectShow).</span><span class="sxs-lookup"><span data-stu-id="2dd25-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="2dd25-118">El uso de los códecs de las series Windows Media Audio y Video 9 a través de los componentes de DirectShow QASF requiere Microsoft Windows Millennium Edition o posterior, o DirectX 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2dd25-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="2dd25-119">En el diagrama siguiente se muestra un gráfico de filtros de DirectShow para reproducir Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="2dd25-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Gráfico de reproducción de vídeo de Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="2dd25-121">El [lector DE ASF](wm-asf-reader-filter.md) wm es un componente QASF, los descodificadores son componentes del SDK de Windows Media Format hospedados en el filtro contenedor de DMO (un componente QASF) y los representadores son componentes de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2dd25-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




