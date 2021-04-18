---
description: La interfaz IStas proporciona los métodos que se usan para conectar un NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red. Esta interfaz genera estadísticas sin fotogramas.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaz IStas (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687000"
---
# <a name="istats-interface"></a><span data-ttu-id="e9442-104">Interfaz IStas</span><span class="sxs-lookup"><span data-stu-id="e9442-104">IStats interface</span></span>

<span data-ttu-id="e9442-105">La interfaz **istas** proporciona los métodos que se usan para conectar un NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="e9442-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="e9442-106">Esta interfaz genera estadísticas sin fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e9442-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="e9442-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9442-107">Members</span></span>

<span data-ttu-id="e9442-108">La interfaz **istas** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e9442-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9442-109">Los **ISTA** también tienen estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e9442-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="e9442-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9442-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9442-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9442-111">Methods</span></span>

<span data-ttu-id="e9442-112">La interfaz **istas** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e9442-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="e9442-113">Método</span><span class="sxs-lookup"><span data-stu-id="e9442-113">Method</span></span>                                                                | <span data-ttu-id="e9442-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9442-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9442-115">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e9442-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="e9442-116">Configura el desencadenador, la coincidencia de patrón y el tamaño del búfer del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e9442-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="e9442-117">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="e9442-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="e9442-118">Conecta el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="e9442-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e9442-119">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="e9442-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="e9442-120">Desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="e9442-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="e9442-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="e9442-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="e9442-122">Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e9442-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="e9442-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="e9442-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="e9442-124">Recupera información de la [*sesión*](s.md) y de la [*estación*](s.md) sobre la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e9442-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="e9442-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="e9442-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="e9442-126">Extrae la hora, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e9442-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="e9442-127">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="e9442-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="e9442-128">Detiene temporalmente la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e9442-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="e9442-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="e9442-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="e9442-130">Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.</span><span class="sxs-lookup"><span data-stu-id="e9442-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="e9442-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="e9442-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="e9442-132">Recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="e9442-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e9442-133">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="e9442-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="e9442-134">Reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="e9442-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="e9442-135">**Start**</span><span class="sxs-lookup"><span data-stu-id="e9442-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="e9442-136">Inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="e9442-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="e9442-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="e9442-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="e9442-138">Detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e9442-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="e9442-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9442-139">Requirements</span></span>



| <span data-ttu-id="e9442-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9442-140">Requirement</span></span> | <span data-ttu-id="e9442-141">Value</span><span class="sxs-lookup"><span data-stu-id="e9442-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9442-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9442-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e9442-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e9442-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e9442-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9442-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e9442-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9442-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e9442-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9442-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9442-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9442-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e9442-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9442-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9442-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9442-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

