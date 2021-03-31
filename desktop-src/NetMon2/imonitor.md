---
description: La interfaz IMonitor proporciona métodos que controlan la operación de supervisión. El servicio de control de supervisión (MCSVC) llama a estos métodos.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaz IMonitor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908301"
---
# <a name="imonitor-interface"></a><span data-ttu-id="9013f-104">Interfaz IMonitor</span><span class="sxs-lookup"><span data-stu-id="9013f-104">IMonitor interface</span></span>

<span data-ttu-id="9013f-105">La interfaz **IMonitor** proporciona métodos que controlan la operación de supervisión.</span><span class="sxs-lookup"><span data-stu-id="9013f-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="9013f-106">El [*servicio de control de supervisión*](m.md) (MCSVC) llama a estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9013f-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="9013f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9013f-107">Members</span></span>

<span data-ttu-id="9013f-108">La interfaz **IMonitor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9013f-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9013f-109">**IMonitor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9013f-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="9013f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9013f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9013f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9013f-111">Methods</span></span>

<span data-ttu-id="9013f-112">La interfaz **IMonitor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9013f-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="9013f-113">Método</span><span class="sxs-lookup"><span data-stu-id="9013f-113">Method</span></span>                                        | <span data-ttu-id="9013f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9013f-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9013f-115">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="9013f-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="9013f-116">Actualiza la configuración del monitor.</span><span class="sxs-lookup"><span data-stu-id="9013f-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="9013f-117">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="9013f-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="9013f-118">Inicializa un monitor.</span><span class="sxs-lookup"><span data-stu-id="9013f-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="9013f-119">**Marcos**</span><span class="sxs-lookup"><span data-stu-id="9013f-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="9013f-120">Indica el estado de un evento de marco.</span><span class="sxs-lookup"><span data-stu-id="9013f-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="9013f-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="9013f-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="9013f-122">Indica que el monitor se ha configurado correctamente y que la captura de datos está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="9013f-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="9013f-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="9013f-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="9013f-124">Indica un evento de estado NPP.</span><span class="sxs-lookup"><span data-stu-id="9013f-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="9013f-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="9013f-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="9013f-126">Indica la finalización de la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="9013f-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="9013f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9013f-127">Requirements</span></span>



| <span data-ttu-id="9013f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9013f-128">Requirement</span></span> | <span data-ttu-id="9013f-129">Value</span><span class="sxs-lookup"><span data-stu-id="9013f-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9013f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9013f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9013f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9013f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9013f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9013f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9013f-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9013f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9013f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9013f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9013f-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9013f-135"><dt>Netmon.h</dt></span></span> </dl> |



 

