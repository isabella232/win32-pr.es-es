---
description: Accesos directos a páginas de referencia de DVD de C++
ms.assetid: b37337b7-b3be-4f49-b350-df5e3c88e3cf
title: Accesos directos a páginas de referencia de DVD de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7caed2aea59e41cf666c6ed63d220f986a8e36
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537564"
---
# <a name="shortcuts-to-c-dvd-reference-pages"></a><span data-ttu-id="6ac7e-103">Accesos directos a páginas de referencia de DVD de C++</span><span class="sxs-lookup"><span data-stu-id="6ac7e-103">Shortcuts to C++ DVD Reference Pages</span></span>

<span data-ttu-id="6ac7e-104">Las siguientes interfaces son las utilizadas normalmente al escribir una aplicación de DVD en C++.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-104">The following interfaces are those typically used when writing a DVD application in C++.</span></span>



| <span data-ttu-id="6ac7e-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6ac7e-105">Interface</span></span>                                    | <span data-ttu-id="6ac7e-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="6ac7e-106">Purpose</span></span>                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ac7e-107">**IAMLine21Decoder**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-107">**IAMLine21Decoder**</span></span>](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) | <span data-ttu-id="6ac7e-108">Controla la presentación de subtítulos.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-108">Controls closed captioning display.</span></span>                                                              |
| [<span data-ttu-id="6ac7e-109">**IDvdCmd**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-109">**IDvdCmd**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)                   | <span data-ttu-id="6ac7e-110">Se utiliza en técnicas avanzadas de sincronización de comandos para controlar un objeto de comando.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-110">Used in advanced command synchronization techniques to control a command object.</span></span>                 |
| [<span data-ttu-id="6ac7e-111">**IDvdControl2**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-111">**IDvdControl2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)         | <span data-ttu-id="6ac7e-112">Emite comandos para el filtro del [navegador de DVD](dvd-navigator-filter.md) (los métodos "SET").</span><span class="sxs-lookup"><span data-stu-id="6ac7e-112">Issues commands to the [DVD Navigator](dvd-navigator-filter.md) filter (the "set" methods).</span></span>     |
| [<span data-ttu-id="6ac7e-113">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-113">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) | <span data-ttu-id="6ac7e-114">Crea el gráfico de filtros de DVD.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-114">Creates the DVD filter graph.</span></span>                                                                    |
| [<span data-ttu-id="6ac7e-115">**IDvdInfo2**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-115">**IDvdInfo2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)               | <span data-ttu-id="6ac7e-116">Consulta el navegador del DVD para obtener información de estado e información sobre el disco (los métodos de "obtención").</span><span class="sxs-lookup"><span data-stu-id="6ac7e-116">Queries the DVD Navigator for state information and information on the disc (the "get" methods).</span></span> |
| [<span data-ttu-id="6ac7e-117">**IDvdState**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-117">**IDvdState**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdstate)               | <span data-ttu-id="6ac7e-118">Guarda la información, como los marcadores, en el disco.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-118">Saves information, such as bookmarks, to disc.</span></span>                                                   |
| [<span data-ttu-id="6ac7e-119">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="6ac7e-119">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)   | <span data-ttu-id="6ac7e-120">Controla el "recorrido de fotogramas" si el descodificador lo admite.</span><span class="sxs-lookup"><span data-stu-id="6ac7e-120">Controls "frame stepping" if the decoder supports it.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="6ac7e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ac7e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ac7e-122">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="6ac7e-122">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



