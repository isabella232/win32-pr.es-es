---
description: Implementado por el explorador. Expone métodos que administran el monitor que contiene la barra de tareas de Windows en un sistema de varios monitores.
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
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997965"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="36fca-104">Interfaz IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="36fca-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="36fca-105">Implementado por el explorador.</span><span class="sxs-lookup"><span data-stu-id="36fca-105">Implemented by the browser.</span></span> <span data-ttu-id="36fca-106">Expone métodos que administran el monitor que contiene la barra de tareas de Windows en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="36fca-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="36fca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="36fca-107">Members</span></span>

<span data-ttu-id="36fca-108">La interfaz **IMultiMonitorDockingSite** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="36fca-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36fca-109">**IMultiMonitorDockingSite** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36fca-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="36fca-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="36fca-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36fca-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="36fca-111">Methods</span></span>

<span data-ttu-id="36fca-112">La interfaz **IMultiMonitorDockingSite** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="36fca-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="36fca-113">Método</span><span class="sxs-lookup"><span data-stu-id="36fca-113">Method</span></span>                                                            | <span data-ttu-id="36fca-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="36fca-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36fca-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="36fca-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="36fca-116">Obtiene el monitor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="36fca-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="36fca-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="36fca-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="36fca-118">Comprueba que el monitor está activo y disponible.</span><span class="sxs-lookup"><span data-stu-id="36fca-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="36fca-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="36fca-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="36fca-120">Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="36fca-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36fca-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36fca-121">Remarks</span></span>

<span data-ttu-id="36fca-122">Normalmente no se implementa la interfaz **IMultiMonitorDockingSite** .</span><span class="sxs-lookup"><span data-stu-id="36fca-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="36fca-123">El explorador de Shell implementa esta interfaz para admitir varios monitores.</span><span class="sxs-lookup"><span data-stu-id="36fca-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fca-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36fca-124">Requirements</span></span>



| <span data-ttu-id="36fca-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="36fca-125">Requirement</span></span> | <span data-ttu-id="36fca-126">Value</span><span class="sxs-lookup"><span data-stu-id="36fca-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="36fca-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36fca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="36fca-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="36fca-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="36fca-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36fca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="36fca-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="36fca-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
