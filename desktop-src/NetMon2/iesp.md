---
description: La interfaz IESP proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaz IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154146"
---
# <a name="iesp-interface"></a><span data-ttu-id="bea00-103">Interfaz IESP</span><span class="sxs-lookup"><span data-stu-id="bea00-103">IESP interface</span></span>

<span data-ttu-id="bea00-104">La interfaz **iesp** proporciona los métodos que conectan el NPP a la red, capturan el tráfico de red a un archivo de captura, recuperan estadísticas y desconectan el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="bea00-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="bea00-105">Esta interfaz se utiliza principalmente cuando necesita recopilar estadísticas de [*conversación*](c.md) de red en un formato de archivo ESP propietario.</span><span class="sxs-lookup"><span data-stu-id="bea00-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="bea00-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bea00-106">Members</span></span>

<span data-ttu-id="bea00-107">La interfaz **iesp** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bea00-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bea00-108">**Iesp** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bea00-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="bea00-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="bea00-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bea00-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bea00-110">Methods</span></span>

<span data-ttu-id="bea00-111">La interfaz **iesp** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bea00-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="bea00-112">Método</span><span class="sxs-lookup"><span data-stu-id="bea00-112">Method</span></span>                                          | <span data-ttu-id="bea00-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bea00-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bea00-114">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="bea00-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="bea00-115">Envía la información de configuración de una captura.</span><span class="sxs-lookup"><span data-stu-id="bea00-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="bea00-116">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="bea00-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="bea00-117">Conecta el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="bea00-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="bea00-118">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="bea00-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="bea00-119">Desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="bea00-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="bea00-120">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="bea00-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="bea00-121">Recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="bea00-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="bea00-122">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="bea00-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="bea00-123">Detiene temporalmente la captura actual.</span><span class="sxs-lookup"><span data-stu-id="bea00-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="bea00-124">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="bea00-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="bea00-125">Recupera una lista de todos los equipos que usan Monitor de red para capturar datos en una subred.</span><span class="sxs-lookup"><span data-stu-id="bea00-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="bea00-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="bea00-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="bea00-127">Recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="bea00-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="bea00-128">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="bea00-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="bea00-129">Reanuda una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="bea00-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="bea00-130">**Start**</span><span class="sxs-lookup"><span data-stu-id="bea00-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="bea00-131">Inicia la captura y crea el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="bea00-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="bea00-132">**Stop**</span><span class="sxs-lookup"><span data-stu-id="bea00-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="bea00-133">Detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="bea00-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="bea00-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea00-134">Requirements</span></span>



| <span data-ttu-id="bea00-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea00-135">Requirement</span></span> | <span data-ttu-id="bea00-136">Value</span><span class="sxs-lookup"><span data-stu-id="bea00-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea00-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea00-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bea00-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bea00-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bea00-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea00-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bea00-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bea00-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bea00-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea00-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea00-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bea00-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bea00-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bea00-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bea00-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bea00-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

