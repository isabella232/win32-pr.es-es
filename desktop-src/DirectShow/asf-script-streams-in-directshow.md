---
description: Secuencias de script ASF en DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Secuencias de script ASF en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997941"
---
# <a name="asf-script-streams-in-directshow"></a><span data-ttu-id="a13f4-103">Secuencias de script ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a13f4-103">ASF Script Streams in DirectShow</span></span>

<span data-ttu-id="a13f4-104">Cuando se proporciona al filtro de [lector ASF de WM](wm-asf-reader-filter.md) un archivo que incluye una secuencia de tipo WMMEDIATYPE \_ script, se crea un PIN de salida para él que se puede conectar al filtro de [representador del comando de script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a13f4-104">When the [WM ASF Reader](wm-asf-reader-filter.md) filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="a13f4-105">Cuando se llama a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ese filtro se agrega automáticamente al gráfico y se conecta.</span><span class="sxs-lookup"><span data-stu-id="a13f4-105">When you call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="a13f4-106">Cuando el representador del comando de script interno recibe un ejemplo que contiene un comando de script, activa un evento de [**\_ \_ evento OLE de EC**](ec-ole-event.md) cuyo *lParam* contiene el script.</span><span class="sxs-lookup"><span data-stu-id="a13f4-106">When the Internal Script Command Renderer receives a sample containing a script command, it fires an [**EC\_OLE\_EVENT**](ec-ole-event.md) event whose *lParam* contains the script.</span></span> <span data-ttu-id="a13f4-107">La aplicación es totalmente responsable de controlar este evento.</span><span class="sxs-lookup"><span data-stu-id="a13f4-107">The application is entirely responsible for handling this event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a13f4-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a13f4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a13f4-109">Leer archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a13f4-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



