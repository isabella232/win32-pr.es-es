---
title: Interfaz IMsRdpInputSink
description: Receptor de entrada de escritorio remoto.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpInputSink
- Servicios de Escritorio remoto de la interfaz IMsRdpInputSink, descrito
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996140"
---
# <a name="imsrdpinputsink-interface"></a><span data-ttu-id="6e404-105">Interfaz IMsRdpInputSink</span><span class="sxs-lookup"><span data-stu-id="6e404-105">IMsRdpInputSink interface</span></span>

<span data-ttu-id="6e404-106">Receptor de entrada de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6e404-106">Remote desktop input sink.</span></span>

## <a name="members"></a><span data-ttu-id="6e404-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e404-107">Members</span></span>

<span data-ttu-id="6e404-108">La interfaz **IMsRdpInputSink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6e404-108">The **IMsRdpInputSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6e404-109">**IMsRdpInputSink** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6e404-109">**IMsRdpInputSink** also has these types of members:</span></span>

-   [<span data-ttu-id="6e404-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e404-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6e404-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e404-111">Methods</span></span>

<span data-ttu-id="6e404-112">La interfaz **IMsRdpInputSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6e404-112">The **IMsRdpInputSink** interface has these methods.</span></span>



| <span data-ttu-id="6e404-113">Método</span><span class="sxs-lookup"><span data-stu-id="6e404-113">Method</span></span>                                                               | <span data-ttu-id="6e404-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e404-114">Description</span></span>                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| <span data-ttu-id="6e404-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-115">[**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))</span></span>               | <span data-ttu-id="6e404-116">Agrega una entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="6e404-116">Adds touch input.</span></span><br/>         |
| <span data-ttu-id="6e404-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-117">[**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))</span></span>           | <span data-ttu-id="6e404-118">Iniciar el marco táctil.</span><span class="sxs-lookup"><span data-stu-id="6e404-118">Begin touch frame.</span></span><br/>        |
| <span data-ttu-id="6e404-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-119">[**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))</span></span>               | <span data-ttu-id="6e404-120">Fin del marco táctil.</span><span class="sxs-lookup"><span data-stu-id="6e404-120">End touch frame.</span></span><br/>          |
| <span data-ttu-id="6e404-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-121">[**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))</span></span>       | <span data-ttu-id="6e404-122">Envía el evento de teclado.</span><span class="sxs-lookup"><span data-stu-id="6e404-122">Sends keyboard event.</span></span><br/>     |
| <span data-ttu-id="6e404-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-123">[**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85))</span></span> | <span data-ttu-id="6e404-124">Envía el evento de botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="6e404-124">Sends mouse button event.</span></span><br/> |
| <span data-ttu-id="6e404-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-125">[**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))</span></span>     | <span data-ttu-id="6e404-126">Envía el evento de movimiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="6e404-126">Sends mouse move event.</span></span><br/>   |
| <span data-ttu-id="6e404-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-127">[**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))</span></span>   | <span data-ttu-id="6e404-128">Envía el evento de rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="6e404-128">Sends mouse wheel event.</span></span><br/>  |
| <span data-ttu-id="6e404-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e404-129">[**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))</span></span>               | <span data-ttu-id="6e404-130">Envía el evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6e404-130">Sends sync event.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="6e404-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e404-131">Requirements</span></span>



| <span data-ttu-id="6e404-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e404-132">Requirement</span></span> | <span data-ttu-id="6e404-133">Value</span><span class="sxs-lookup"><span data-stu-id="6e404-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e404-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e404-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6e404-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e404-135">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="6e404-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e404-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6e404-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6e404-137">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="6e404-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e404-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e404-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e404-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e404-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e404-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e404-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e404-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e404-142">IID</span><span class="sxs-lookup"><span data-stu-id="6e404-142">IID</span></span><br/>                      | <span data-ttu-id="6e404-143">IID \_ IMsRdpInputSink se define como 4606850E-76A7-4E28-A47E-C7174F619351</span><span class="sxs-lookup"><span data-stu-id="6e404-143">IID\_IMsRdpInputSink is defined as 4606850E-76A7-4E28-A47E-C7174F619351</span></span><br/>     |



 

