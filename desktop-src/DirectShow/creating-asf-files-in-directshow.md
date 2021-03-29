---
description: Crear archivos ASF en DirectShow
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Crear archivos ASF en DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666149"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="89f62-103">Crear archivos ASF en DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="89f62-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="89f62-104">En esta sección se describe cómo usar el filtro de [escritor ASF](wm-asf-writer-filter.md) de DirectShow para crear archivos en el formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="89f62-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="89f62-105">ASF es un formato de contenedor que puede contener cualquier tipo de datos comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="89f62-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="89f62-106">Los archivos de formato de Windows Media son archivos ASF que usan determinados códecs, tal como se especifica en el kit de desarrollo de software (SDK) de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="89f62-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="89f62-107">Estos archivos usan las extensiones ". WMA" para los archivos de Windows Media Audio y ". WMV" para los archivos de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="89f62-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="89f62-108">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="89f62-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="89f62-109">El SDK de DirectShow y el SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="89f62-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="89f62-110">Configuración del escritor ASF</span><span class="sxs-lookup"><span data-stu-id="89f62-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="89f62-111">Generar gráficos de filtro para escribir archivos ASF</span><span class="sxs-lookup"><span data-stu-id="89f62-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="89f62-112">Configuración de perfiles y otras propiedades de archivo ASF</span><span class="sxs-lookup"><span data-stu-id="89f62-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="89f62-113">Desbloqueo del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="89f62-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="89f62-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89f62-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f62-115">Usar Windows Media en DirectShow</span><span class="sxs-lookup"><span data-stu-id="89f62-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



