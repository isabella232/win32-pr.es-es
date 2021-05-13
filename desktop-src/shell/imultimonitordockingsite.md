---
description: Implementado por el explorador. Expone métodos que administran qué monitor contiene la barra de tareas de Windows en un sistema de varios monitores.
title: Interfaz IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841896"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="5d1d9-104">Interfaz IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="5d1d9-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="5d1d9-105">Implementado por el explorador.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-105">Implemented by the browser.</span></span> <span data-ttu-id="5d1d9-106">Expone métodos que administran qué monitor contiene la barra de tareas de Windows en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="5d1d9-107">Members</span><span class="sxs-lookup"><span data-stu-id="5d1d9-107">Members</span></span>

<span data-ttu-id="5d1d9-108">La **interfaz IMultiMonitorDockingSite** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="5d1d9-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d1d9-109">**IMultiMonitorDockingSite** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d1d9-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="5d1d9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d1d9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d1d9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d1d9-111">Methods</span></span>

<span data-ttu-id="5d1d9-112">La **interfaz IMultiMonitorDockingSite** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="5d1d9-113">Método</span><span class="sxs-lookup"><span data-stu-id="5d1d9-113">Method</span></span>                                                            | <span data-ttu-id="5d1d9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d1d9-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d1d9-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="5d1d9-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="5d1d9-116">Obtiene el monitor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="5d1d9-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="5d1d9-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="5d1d9-118">Comprueba que el monitor está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="5d1d9-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="5d1d9-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="5d1d9-120">Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d1d9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d1d9-121">Remarks</span></span>

<span data-ttu-id="5d1d9-122">Normalmente no se implementa la **interfaz IMultiMonitorDockingSite.**</span><span class="sxs-lookup"><span data-stu-id="5d1d9-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="5d1d9-123">El explorador shell implementa esta interfaz para admitir varios monitores.</span><span class="sxs-lookup"><span data-stu-id="5d1d9-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1d9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d1d9-124">Requirements</span></span>



| <span data-ttu-id="5d1d9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d1d9-125">Requirement</span></span> | <span data-ttu-id="5d1d9-126">Value</span><span class="sxs-lookup"><span data-stu-id="5d1d9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5d1d9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d1d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d1d9-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="5d1d9-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d1d9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d1d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d1d9-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d1d9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
