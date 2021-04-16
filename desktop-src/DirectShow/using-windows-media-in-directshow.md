---
description: Usar Windows Media en DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Usar Windows Media en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424127"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="02a8d-103">Usar Windows Media en DirectShow</span><span class="sxs-lookup"><span data-stu-id="02a8d-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="02a8d-104">En esta sección se describe cómo usar DirectShow para reproducir y escribir archivos Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="02a8d-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="02a8d-105">Los archivos ASF suelen contener contenido de audio y vídeo codificado mediante los códecs de vídeo y Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="02a8d-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="02a8d-106">Sin embargo, ASF puede contener cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="02a8d-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="02a8d-107">Los filtros DirectShow siguientes admiten la lectura y escritura de archivos ASF:</span><span class="sxs-lookup"><span data-stu-id="02a8d-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="02a8d-108">[Filtro de lector ASF de WM](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="02a8d-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="02a8d-109">Lee archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="02a8d-109">Reads ASF files.</span></span>
-   <span data-ttu-id="02a8d-110">[Filtro del escritor ASF de WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="02a8d-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="02a8d-111">Archivos ASF de Wrties.</span><span class="sxs-lookup"><span data-stu-id="02a8d-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="02a8d-112">[Filtro de contenedor de DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="02a8d-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="02a8d-113">Incluye el codificador y descodificador de Windows Media DMOs.</span><span class="sxs-lookup"><span data-stu-id="02a8d-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="02a8d-114">Versiones</span><span class="sxs-lookup"><span data-stu-id="02a8d-114">Versions</span></span>

<span data-ttu-id="02a8d-115">Los filtros del lector ASF de WM y del escritor ASF de WM se empaquetan en el archivo DLL denominado qasf.dll y los filtros se denominan colectivamente "componentes QASF".</span><span class="sxs-lookup"><span data-stu-id="02a8d-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="02a8d-116">Estos filtros son contenedores del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="02a8d-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="02a8d-117">El archivo DLL (qasf.dll) se publicó por primera vez en el SDK de DirectX, pero se actualizó posteriormente en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="02a8d-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="02a8d-118">Este es el historial de versiones de los filtros de QASF:</span><span class="sxs-lookup"><span data-stu-id="02a8d-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="02a8d-119">DirectShow 8,1 es compatible con Windows Media Format SDK versión 7,0.</span><span class="sxs-lookup"><span data-stu-id="02a8d-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="02a8d-120">DirectShow 9,0 es compatible con Windows Media Format SDK versión 7,1.</span><span class="sxs-lookup"><span data-stu-id="02a8d-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="02a8d-121">Windows XP Service Pack 2 es compatible con Windows Media Format 9 SDK.</span><span class="sxs-lookup"><span data-stu-id="02a8d-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="02a8d-122">Windows Vista es compatible con Windows Media Format 11 SDK.</span><span class="sxs-lookup"><span data-stu-id="02a8d-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="02a8d-123">Windows Media Format 9 SDK y versiones posteriores contienen las versiones correspondientes de QASF.</span><span class="sxs-lookup"><span data-stu-id="02a8d-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="02a8d-124">Para obtener la versión más reciente de QASF, Descargue siempre el SDK de Windows Media Format más reciente.</span><span class="sxs-lookup"><span data-stu-id="02a8d-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="02a8d-125">Filtro de origen de Windows Media heredado</span><span class="sxs-lookup"><span data-stu-id="02a8d-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="02a8d-126">En Windows XP Service Pack 1 y versiones anteriores, el filtro de origen predeterminado para los archivos ASF (extensiones de archivo. ASF,. WMV y. WMA) es el filtro de origen obsoleto de [Windows Media](windows-media-source-filter.md).</span><span class="sxs-lookup"><span data-stu-id="02a8d-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="02a8d-127">Este comportamiento se mantuvo para garantizar la compatibilidad con versiones anteriores de las aplicaciones que usaban Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="02a8d-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="02a8d-128">Las nuevas aplicaciones deben usar las versiones más recientes de QASF, que hacen que el lector ASF de WM filtre el filtro predeterminado para reproducir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="02a8d-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="02a8d-129">Para obtener más información sobre el conjunto de aplicaciones de Windows Media de kits de desarrollo de software, consulte la sección [audio y vídeo](../audio-and-video.md) de la biblioteca MDSN.</span><span class="sxs-lookup"><span data-stu-id="02a8d-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="02a8d-130">Ese artículo contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="02a8d-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="02a8d-131">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="02a8d-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="02a8d-132">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="02a8d-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="02a8d-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02a8d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a8d-134">Usar DirectShow</span><span class="sxs-lookup"><span data-stu-id="02a8d-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
