---
title: Acerca de DirectShow (Windows Media Format 11 SDK)
description: Acerca de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078753"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="abe06-107">Acerca de DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="abe06-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="abe06-108">DirectShow es una arquitectura de streaming de datos de alto nivel, modular y extensible para la plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="abe06-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="abe06-109">Proporciona los componentes de software subyacentes y las interfaces de programación de aplicaciones (API) para una amplia variedad de aplicaciones de audio y vídeo digitales en el mercado de hoy en día.</span><span class="sxs-lookup"><span data-stu-id="abe06-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="abe06-110">DirectShow está disponible como parte del kit de desarrollo de software de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="abe06-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="abe06-111">Para obtener más información sobre DirectShow, vea el SDK de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="abe06-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="abe06-112">En DirectShow, todos los componentes de streaming de datos se denominan *filtros*.</span><span class="sxs-lookup"><span data-stu-id="abe06-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="abe06-113">Un filtro puede representar un dispositivo de hardware, un codificador o descodificador de software, un representador de audio o vídeo o cualquier capacidad de procesamiento de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="abe06-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="abe06-114">Para permitir que las aplicaciones basadas en DirectShow lean y escriban contenido de formato de Windows Media, incluido el contenido protegido por Rights Management digitales (DRM), Microsoft proporciona dos filtros que encapsulan partes del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="abe06-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="abe06-115">Estos son el [lector ASF de WM](wm-asf-reader-filter.md) y el [escritor ASF de WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="abe06-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="abe06-116">Estos filtros y las interfaces que exponen se conocen colectivamente como componentes de QASF, después de la DLL en la que se empaquetan.</span><span class="sxs-lookup"><span data-stu-id="abe06-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="abe06-117">(La letra Q significa Quartz, un nombre de código temprano para DirectShow).</span><span class="sxs-lookup"><span data-stu-id="abe06-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="abe06-118">El uso de los códecs de la serie de Windows Media Audio y vídeo 9 a través de los componentes de QASF de DirectShow requiere Microsoft Windows Millennium Edition o posterior, o bien DirectX 8,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="abe06-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="abe06-119">En el diagrama siguiente se muestra un gráfico de filtros de DirectShow para reproducir archivos Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="abe06-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![gráfico de reproducción de vídeo de Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="abe06-121">El [lector ASF de WM](wm-asf-reader-filter.md) es un componente de qasf, los descodificadores son componentes del SDK de Windows Media Format hospedados en el filtro de contenedor de DMO (un componente qasf) y los representadores son componentes de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="abe06-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




