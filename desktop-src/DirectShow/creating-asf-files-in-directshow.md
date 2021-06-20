---
description: Obtenga información sobre cómo crear archivos ASF en DirectShow. ASF es un formato de contenedor que puede contener cualquier tipo de datos.
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Creación de archivos ASF en DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4614ed813c2e9f51c77cd8773739188aa5d4d07
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403969"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="b8390-104">Creación de archivos ASF en DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b8390-104">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="b8390-105">En esta sección se describe cómo usar el filtro [ASF Writer](wm-asf-writer-filter.md) de DirectShow WM para crear archivos en formato de sistemas avanzados (ASF).</span><span class="sxs-lookup"><span data-stu-id="b8390-105">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="b8390-106">ASF es un formato de contenedor que puede contener cualquier tipo de datos comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b8390-106">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="b8390-107">Windows Media Format archivos son archivos ASF que usan determinados códecs, tal y como se especifica en Windows Media Format Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b8390-107">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="b8390-108">Estos archivos usan las extensiones ".wma" para Windows Media Audio archivos y ".wmv" para Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="b8390-108">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="b8390-109">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="b8390-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b8390-110">El SDK de DirectShow y Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="b8390-110">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="b8390-111">Configuración del escritor de ASF</span><span class="sxs-lookup"><span data-stu-id="b8390-111">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="b8390-112">Creación de gráficos de filtro para escribir archivos ASF</span><span class="sxs-lookup"><span data-stu-id="b8390-112">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="b8390-113">Configuración de perfiles y otras propiedades de archivo ASF</span><span class="sxs-lookup"><span data-stu-id="b8390-113">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="b8390-114">Desbloqueo del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="b8390-114">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="b8390-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8390-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8390-116">Uso de Windows Media en DirectShow</span><span class="sxs-lookup"><span data-stu-id="b8390-116">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



