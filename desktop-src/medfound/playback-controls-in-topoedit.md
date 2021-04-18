---
description: Controles de reproducción en TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reproducción en TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564847"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="e037c-103">Controles de reproducción en TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e037c-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="e037c-104">Una vez que se resuelve una topología, se pone en cola en la sesión multimedia para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e037c-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="e037c-105">TopoEdit proporciona control de transporte para cambiar el estado de la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="e037c-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="e037c-106">En la tabla siguiente se muestra el comando de menú/barra de herramientas y el método de Media Foundation equivalente para cada operación.</span><span class="sxs-lookup"><span data-stu-id="e037c-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="e037c-107">Comando de menú/barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="e037c-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="e037c-108">Método Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e037c-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e037c-109">En el menú **controles** , haga clic en **reproducir**. \[ nueva línea \] : o bien, \[ \] haga clic en el botón **reproducir** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón reproducir](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="e037c-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="e037c-110">**IMFMediaSession:: Start**</span><span class="sxs-lookup"><span data-stu-id="e037c-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="e037c-111">En el menú **controles** , haga clic en **detener**. \[ nueva línea \] -o- \[ nueva línea \] haga clic en el botón **detener** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón detener](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="e037c-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="e037c-112">**IMFMediaSession:: Stop**</span><span class="sxs-lookup"><span data-stu-id="e037c-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="e037c-113">En el menú **controles** , haga clic en **pausar**. \[ nueva línea \] : o bien, \[ \] haga clic en el botón **pausar** de la barra de herramientas (se muestra en la siguiente imagen). \[ \] ![ captura de pantalla de nueva línea del botón pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="e037c-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="e037c-114">**IMFMediaSession::P ause**</span><span class="sxs-lookup"><span data-stu-id="e037c-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="e037c-115">Para obtener información sobre cómo controlar la reproducción mediante programación con Media Foundation API, vea [Cómo controlar los Estados de presentación](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="e037c-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="e037c-116">Invoca</span><span class="sxs-lookup"><span data-stu-id="e037c-116">Seeking</span></span>

<span data-ttu-id="e037c-117">Si se puede buscar en la topología, puede buscar mediante la barra de búsqueda (que se muestra en la imagen siguiente) para especificar un lugar en la escala de tiempo de la topología para comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e037c-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![captura de pantalla de la barra de búsqueda](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="e037c-119">Si se puede buscar en el origen de medios, el comando STOP también busca la topología en el inicio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e037c-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="e037c-120">Cambiar la velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="e037c-120">Changing the Playback Rate</span></span>

<span data-ttu-id="e037c-121">Si el origen de medios subyacentes de la topología admite varias velocidades de reproducción, puede usar la barra de frecuencia para cambiar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e037c-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="e037c-122">Para avanzar rápidamente una topología en la sesión multimedia, aumente la velocidad arrastrando el control deslizante hacia la derecha, tal como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="e037c-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![captura de pantalla de la barra de tasa](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="e037c-124">En esta versión, TopoEdit solo admite tarifas positivas.</span><span class="sxs-lookup"><span data-stu-id="e037c-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="e037c-125">No se admite la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="e037c-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="e037c-126">Para obtener información sobre cómo cambiar la velocidad de reproducción mediante programación con Media Foundation API, vea [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="e037c-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e037c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e037c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e037c-128">Menús de TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e037c-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="e037c-129">Barra de herramientas TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e037c-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="e037c-130">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e037c-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



