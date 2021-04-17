---
description: API de vídeo de Direct3D 9
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: API de vídeo de Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539568"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="c6b31-103">API de vídeo de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="c6b31-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6b31-104">Las aplicaciones de la tienda Windows deben usar Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="c6b31-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c6b31-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c6b31-105">In this section</span></span>



| <span data-ttu-id="c6b31-106">Tema</span><span class="sxs-lookup"><span data-stu-id="c6b31-106">Topic</span></span>                                                                       | <span data-ttu-id="c6b31-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6b31-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6b31-108">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="c6b31-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="c6b31-109">Describe el contenido de vídeo: capacidades de protección que puede proporcionar un controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c6b31-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="c6b31-110">Compatibilidad con la superposición de hardware</span><span class="sxs-lookup"><span data-stu-id="c6b31-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="c6b31-111">Describe cómo usar superposiciones de hardware en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c6b31-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="c6b31-112">Informes de presión de memoria</span><span class="sxs-lookup"><span data-stu-id="c6b31-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="c6b31-113">Los informes de presión de memoria permiten a una aplicación de Direct3D determinar si el espacio de trabajo de la memoria de vídeo ha crecido demasiado.</span><span class="sxs-lookup"><span data-stu-id="c6b31-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="c6b31-114">Interfaces de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c6b31-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="c6b31-115">Describe las interfaces de vídeo de Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c6b31-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="c6b31-116">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c6b31-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="c6b31-117">Describe las estructuras que usan las interfaces de vídeo de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c6b31-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="c6b31-118">Enumeraciones de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c6b31-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="c6b31-119">Describe las enumeraciones usadas por las interfaces de vídeo de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c6b31-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="c6b31-120">Content Protection comandos</span><span class="sxs-lookup"><span data-stu-id="c6b31-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="c6b31-121">Enumera los comandos para el método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="c6b31-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="c6b31-122">Consultas Content Protection</span><span class="sxs-lookup"><span data-stu-id="c6b31-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="c6b31-123">Muestra las consultas para el método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="c6b31-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="c6b31-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6b31-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b31-125">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6b31-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




