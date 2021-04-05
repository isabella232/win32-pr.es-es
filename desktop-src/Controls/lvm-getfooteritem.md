---
title: Mensaje de LVM_GETFOOTERITEM (commctrl. h)
description: Obtiene información sobre un elemento de pie de página en un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterItem de ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078864"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="60b74-105">\_Mensaje GETFOOTERITEM LVM</span><span class="sxs-lookup"><span data-stu-id="60b74-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="60b74-106">Obtiene información sobre un elemento de pie de página en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="60b74-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="60b74-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .</span><span class="sxs-lookup"><span data-stu-id="60b74-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="60b74-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60b74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b74-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60b74-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b74-110">Índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="60b74-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="60b74-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60b74-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b74-112">Un puntero a una estructura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para recibir un valor para los miembros **State** y/o **miembros pszText** según el valor del miembro **Mask** .</span><span class="sxs-lookup"><span data-stu-id="60b74-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="60b74-113">El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros para indicar al receptor qué información se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="60b74-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="60b74-114">Para obtener más información, vea **LVFOOTERITEM**.</span><span class="sxs-lookup"><span data-stu-id="60b74-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b74-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60b74-115">Return value</span></span>

<span data-ttu-id="60b74-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="60b74-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b74-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b74-117">Requirements</span></span>



| <span data-ttu-id="60b74-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b74-118">Requirement</span></span> | <span data-ttu-id="60b74-119">Value</span><span class="sxs-lookup"><span data-stu-id="60b74-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b74-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60b74-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="60b74-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60b74-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60b74-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="60b74-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60b74-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60b74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b74-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b74-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





