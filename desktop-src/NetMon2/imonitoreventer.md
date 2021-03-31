---
description: La interfaz IMonitorEventer proporciona métodos para enviar eventos y asignar y liberar recursos de supervisión.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaz IMonitorEventer (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907871"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="a0642-103">Interfaz IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="a0642-103">IMonitorEventer interface</span></span>

<span data-ttu-id="a0642-104">La interfaz **IMonitorEventer** proporciona métodos para enviar eventos y asignar y liberar recursos de supervisión.</span><span class="sxs-lookup"><span data-stu-id="a0642-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="a0642-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0642-105">Members</span></span>

<span data-ttu-id="a0642-106">La interfaz **IMonitorEventer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0642-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0642-107">**IMonitorEventer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0642-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="a0642-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0642-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0642-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0642-109">Methods</span></span>

<span data-ttu-id="a0642-110">La interfaz **IMonitorEventer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a0642-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="a0642-111">Método</span><span class="sxs-lookup"><span data-stu-id="a0642-111">Method</span></span>                                                 | <span data-ttu-id="a0642-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0642-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="a0642-113">**FreeEventData**</span><span class="sxs-lookup"><span data-stu-id="a0642-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="a0642-114">Libera el espacio asignado para los datos del monitor.</span><span class="sxs-lookup"><span data-stu-id="a0642-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="a0642-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="a0642-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="a0642-116">Asigna espacio para supervisar los datos.</span><span class="sxs-lookup"><span data-stu-id="a0642-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="a0642-117">**SendNMEvent**</span><span class="sxs-lookup"><span data-stu-id="a0642-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="a0642-118">Envía eventos a WMI.</span><span class="sxs-lookup"><span data-stu-id="a0642-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="a0642-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0642-119">Requirements</span></span>



| <span data-ttu-id="a0642-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0642-120">Requirement</span></span> | <span data-ttu-id="a0642-121">Value</span><span class="sxs-lookup"><span data-stu-id="a0642-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0642-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0642-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a0642-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a0642-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0642-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0642-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a0642-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0642-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a0642-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0642-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0642-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0642-127"><dt>Netmon.h</dt></span></span> </dl> |



 

