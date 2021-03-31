---
title: Mensaje de LVM_GETFOOTERINFO (commctrl. h)
description: Obtiene información sobre el pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterInfo de ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- LVM_GETFOOTERINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995939"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="85a50-105">\_Mensaje GETFOOTERINFO LVM</span><span class="sxs-lookup"><span data-stu-id="85a50-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="85a50-106">Obtiene información sobre el pie de página de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="85a50-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="85a50-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .</span><span class="sxs-lookup"><span data-stu-id="85a50-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="85a50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85a50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a50-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85a50-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85a50-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="85a50-110">Not used.</span></span> <span data-ttu-id="85a50-111">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="85a50-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="85a50-112">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85a50-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85a50-113">Un puntero a una estructura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) para recibir información según el valor del miembro de **máscara** .</span><span class="sxs-lookup"><span data-stu-id="85a50-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="85a50-114">El proceso de llamada es responsable de asignar esta estructura y establecer el miembro de la **máscara** .</span><span class="sxs-lookup"><span data-stu-id="85a50-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a50-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85a50-115">Return value</span></span>

<span data-ttu-id="85a50-116">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="85a50-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a50-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85a50-117">Requirements</span></span>



| <span data-ttu-id="85a50-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a50-118">Requirement</span></span> | <span data-ttu-id="85a50-119">Value</span><span class="sxs-lookup"><span data-stu-id="85a50-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85a50-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85a50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85a50-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85a50-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85a50-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85a50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85a50-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85a50-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85a50-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85a50-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="85a50-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85a50-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





