---
description: Las marcas siguientes especifican el nivel de reconexión dinámica que se va a usar durante la representación.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Marcas de reconexión dinámica (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679429"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="29555-103">Marcas de reconexión dinámica</span><span class="sxs-lookup"><span data-stu-id="29555-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="29555-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="29555-104">\[Deprecated.</span></span> <span data-ttu-id="29555-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29555-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="29555-106">Las marcas siguientes especifican el nivel de reconexión dinámica que se va a usar durante la representación.</span><span class="sxs-lookup"><span data-stu-id="29555-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="29555-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="29555-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="29555-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="29555-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="29555-109"><dt>**CONNECTF \_ DYNAMIC \_ None**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="29555-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="29555-110">Sin reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="29555-110">No dynamic reconnection.</span></span> <span data-ttu-id="29555-111">Cargue todo antes de representar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="29555-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="29555-112"><dt>**CONNECTF \_ \_Orígenes dinámicos**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="29555-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="29555-113">Cargar solo los orígenes según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29555-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="29555-114"><dt>**CONNECTF \_ \_Efectos dinámicos**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="29555-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="29555-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="29555-115">Reserved.</span></span> <span data-ttu-id="29555-116">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="29555-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="29555-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29555-117">Requirements</span></span>



| <span data-ttu-id="29555-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29555-118">Requirement</span></span> | <span data-ttu-id="29555-119">Value</span><span class="sxs-lookup"><span data-stu-id="29555-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29555-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29555-120">Header</span></span><br/> | <dl> <span data-ttu-id="29555-121"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="29555-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29555-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="29555-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29555-123">**IRenderEngine::SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="29555-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




