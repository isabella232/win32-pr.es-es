---
title: Mensaje de LVM_GETGROUPSTATE (commctrl. h)
description: Obtiene el estado de un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupState de ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489268"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="5511b-105">\_Mensaje GETGROUPSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="5511b-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="5511b-106">Obtiene el estado de un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="5511b-106">Gets the state for a specified group.</span></span> <span data-ttu-id="5511b-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .</span><span class="sxs-lookup"><span data-stu-id="5511b-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5511b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5511b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5511b-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5511b-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5511b-110">Especifica el grupo por **iGroupId** (vea la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="5511b-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="5511b-111">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5511b-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5511b-112">Especifica los valores de estado que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5511b-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="5511b-113">Se trata de una combinación de las marcas enumeradas para el miembro de **Estado** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span><span class="sxs-lookup"><span data-stu-id="5511b-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5511b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5511b-114">Return value</span></span>

<span data-ttu-id="5511b-115">Devuelve la combinación de valores de estado que se establecen.</span><span class="sxs-lookup"><span data-stu-id="5511b-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="5511b-116">Por ejemplo, si *lParam* es LVGS \_ contraído y el valor devuelto es cero, el \_ Estado contraído LVGS no se establece.</span><span class="sxs-lookup"><span data-stu-id="5511b-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="5511b-117">Si no se encuentra el grupo, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5511b-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="5511b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5511b-118">Requirements</span></span>



| <span data-ttu-id="5511b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5511b-119">Requirement</span></span> | <span data-ttu-id="5511b-120">Value</span><span class="sxs-lookup"><span data-stu-id="5511b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5511b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5511b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5511b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5511b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5511b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5511b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5511b-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5511b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5511b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5511b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5511b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5511b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





