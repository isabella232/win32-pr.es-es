---
description: La interfaz IDelaydC proporciona los métodos que se usan para conectarse a la red, capturar el tráfico de red a un archivo de captura, recuperar estadísticas y desconectarse de la red.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interfaz IDelaydC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687086"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="e1cca-103">Interfaz IDelaydC</span><span class="sxs-lookup"><span data-stu-id="e1cca-103">IDelaydC interface</span></span>

<span data-ttu-id="e1cca-104">La interfaz **IDelaydC** proporciona los métodos que se usan para conectarse a la red, capturar el tráfico de red a un archivo de captura, recuperar estadísticas y desconectarse de la red.</span><span class="sxs-lookup"><span data-stu-id="e1cca-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="e1cca-105">Esta interfaz captura fotogramas del flujo de datos de red y, a continuación, copia los fotogramas en un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e1cca-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="e1cca-106">Esta interfaz la usan las aplicaciones Monitor de red y NPP.</span><span class="sxs-lookup"><span data-stu-id="e1cca-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="e1cca-107">Para recibir los datos de red, la NIC de destino debe ser compatible con el modo promiscuo.</span><span class="sxs-lookup"><span data-stu-id="e1cca-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="e1cca-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1cca-108">Members</span></span>

<span data-ttu-id="e1cca-109">La interfaz **IDelaydC** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e1cca-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1cca-110">**IDelaydC** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e1cca-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="e1cca-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1cca-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1cca-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1cca-112">Methods</span></span>

<span data-ttu-id="e1cca-113">La interfaz **IDelaydC** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e1cca-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="e1cca-114">Método</span><span class="sxs-lookup"><span data-stu-id="e1cca-114">Method</span></span>                                                                  | <span data-ttu-id="e1cca-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1cca-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1cca-116">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e1cca-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="e1cca-117">Envía la información de configuración utilizada para una captura.</span><span class="sxs-lookup"><span data-stu-id="e1cca-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="e1cca-118">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="e1cca-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="e1cca-119">Conecta el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="e1cca-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="e1cca-120">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="e1cca-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="e1cca-121">Desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="e1cca-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="e1cca-122">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="e1cca-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="e1cca-123">Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e1cca-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="e1cca-124">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="e1cca-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="e1cca-125">Recupera información de la [*sesión*](s.md) y de la [*estación*](s.md) de la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e1cca-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="e1cca-126">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="e1cca-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="e1cca-127">Extrae la hora, el búfer, el controlador y otras estadísticas de red de la captura que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e1cca-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="e1cca-128">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="e1cca-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="e1cca-129">Detiene temporalmente la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e1cca-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="e1cca-130">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="e1cca-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="e1cca-131">Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.</span><span class="sxs-lookup"><span data-stu-id="e1cca-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="e1cca-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="e1cca-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="e1cca-133">Recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="e1cca-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="e1cca-134">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="e1cca-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="e1cca-135">Reanuda una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="e1cca-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e1cca-136">**Start**</span><span class="sxs-lookup"><span data-stu-id="e1cca-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="e1cca-137">Inicia una captura y crea el [*archivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="e1cca-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="e1cca-138">**Stop**</span><span class="sxs-lookup"><span data-stu-id="e1cca-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="e1cca-139">Detiene la captura actual y cierra el [*archivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="e1cca-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="e1cca-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1cca-140">Requirements</span></span>



| <span data-ttu-id="e1cca-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1cca-141">Requirement</span></span> | <span data-ttu-id="e1cca-142">Value</span><span class="sxs-lookup"><span data-stu-id="e1cca-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cca-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1cca-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e1cca-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1cca-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e1cca-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1cca-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e1cca-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1cca-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e1cca-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1cca-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1cca-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cca-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e1cca-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1cca-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1cca-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1cca-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

