---
description: La interfaz IRTC proporciona los métodos que se usan para conectar el NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interfaz IRTC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001598"
---
# <a name="irtc-interface"></a><span data-ttu-id="c8387-103">Interfaz IRTC</span><span class="sxs-lookup"><span data-stu-id="c8387-103">IRTC interface</span></span>

<span data-ttu-id="c8387-104">La interfaz **IRTC** proporciona los métodos que se usan para conectar el NPP a la red, capturar el tráfico de red, recuperar estadísticas y desconectar el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="c8387-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="c8387-105">**IRTC** obtiene una interfaz a puntos de entrada solo locales, que son necesarios para realizar la captura en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="c8387-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="c8387-106">Esta interfaz incluye un método que entrega una devolución de llamada a NPP.</span><span class="sxs-lookup"><span data-stu-id="c8387-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="c8387-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8387-107">Members</span></span>

<span data-ttu-id="c8387-108">La interfaz **IRTC** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c8387-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8387-109">**IRTC** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8387-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="c8387-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8387-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8387-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8387-111">Methods</span></span>

<span data-ttu-id="c8387-112">La interfaz **IRTC** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c8387-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="c8387-113">Método</span><span class="sxs-lookup"><span data-stu-id="c8387-113">Method</span></span>                                                              | <span data-ttu-id="c8387-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8387-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8387-115">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="c8387-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="c8387-116">Establece el desencadenador, la coincidencia de patrón y el tamaño de búfer de la captura.</span><span class="sxs-lookup"><span data-stu-id="c8387-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="c8387-117">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="c8387-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="c8387-118">Conecta el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="c8387-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c8387-119">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="c8387-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="c8387-120">Desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="c8387-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c8387-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="c8387-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="c8387-122">Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="c8387-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="c8387-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c8387-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="c8387-124">Recupera información de la [*sesión*](s.md) y de la [*estación*](s.md) de la captura actual.</span><span class="sxs-lookup"><span data-stu-id="c8387-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="c8387-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="c8387-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="c8387-126">Extrae la hora, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="c8387-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="c8387-127">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="c8387-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="c8387-128">Detiene temporalmente la captura actual.</span><span class="sxs-lookup"><span data-stu-id="c8387-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c8387-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="c8387-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="c8387-130">Recupera una lista de todos los equipos de una subred que usan Monitor de red para capturar datos de red.</span><span class="sxs-lookup"><span data-stu-id="c8387-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="c8387-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="c8387-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="c8387-132">Recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="c8387-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c8387-133">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="c8387-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="c8387-134">Reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="c8387-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c8387-135">**Start**</span><span class="sxs-lookup"><span data-stu-id="c8387-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="c8387-136">Inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="c8387-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="c8387-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="c8387-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="c8387-138">Detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="c8387-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="c8387-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8387-139">Requirements</span></span>



| <span data-ttu-id="c8387-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8387-140">Requirement</span></span> | <span data-ttu-id="c8387-141">Value</span><span class="sxs-lookup"><span data-stu-id="c8387-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8387-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8387-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c8387-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8387-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c8387-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8387-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c8387-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8387-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c8387-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8387-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8387-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8387-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c8387-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8387-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8387-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8387-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

