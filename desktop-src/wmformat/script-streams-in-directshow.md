---
title: Secuencias de comandos en DirectShow
description: Secuencias de comandos en DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- DirectShow, secuencias de scripts
- secuencias de scripts, DirectShow
- secuencias, secuencias de scripts en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357646"
---
# <a name="script-streams-in-directshow"></a><span data-ttu-id="fe521-112">Secuencias de comandos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fe521-112">Script Streams in DirectShow</span></span>

<span data-ttu-id="fe521-113">Cuando se proporciona al filtro de lector ASF de WM un archivo que incluye una secuencia de tipo WMMEDIATYPE \_ script, se crea un PIN de salida para él que se puede conectar al filtro de representador de comandos de script interno de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fe521-113">When the WM ASF Reader filter is given a file that includes a stream of type WMMEDIATYPE\_Script, it creates an output pin for it that can be connected to the DirectShow Internal Script Command Renderer filter.</span></span> <span data-ttu-id="fe521-114">Cuando se llama a **IGraphBuilder:: RenderFile**, ese filtro se agrega automáticamente al gráfico y se conecta.</span><span class="sxs-lookup"><span data-stu-id="fe521-114">When you call **IGraphBuilder::RenderFile**, that filter is automatically added to the graph and connected.</span></span> <span data-ttu-id="fe521-115">Cuando el representador del comando de script interno recibe un ejemplo que contiene un comando de script, desencadena un **\_ \_ evento OLE de EC** cuyo **lParam** contiene el script.</span><span class="sxs-lookup"><span data-stu-id="fe521-115">When the Internal Script Command Renderer receives a sample containing a script command, it fires an **EC\_OLE\_EVENT** whose **lParam** contains the script.</span></span> <span data-ttu-id="fe521-116">La aplicación es totalmente responsable de controlar este evento.</span><span class="sxs-lookup"><span data-stu-id="fe521-116">The application is entirely responsible for handling this event.</span></span> <span data-ttu-id="fe521-117">Para obtener más información sobre el **\_ \_ evento OLE de EC**, vea la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fe521-117">For more information on **EC\_OLE\_EVENT**, see the DirectShow SDK documentation.</span></span>

 

 




