---
title: Mensaje de LVM_SETITEMSTATE (commctrl. h)
description: Cambia el estado de un elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemState de ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150367"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="1e482-105">\_Mensaje SETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="1e482-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="1e482-106">Cambia el estado de un elemento en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1e482-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="1e482-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .</span><span class="sxs-lookup"><span data-stu-id="1e482-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e482-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e482-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e482-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e482-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e482-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1e482-110">Index of the list-view item.</span></span> <span data-ttu-id="1e482-111">Si este parámetro es-1, el cambio de estado se aplica a todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="1e482-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="1e482-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e482-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e482-113">Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="1e482-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="1e482-114">El miembro **stateMask** especifica qué bits de estado cambiar y el miembro **State** contiene los nuevos valores de esos bits.</span><span class="sxs-lookup"><span data-stu-id="1e482-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="1e482-115">Se omiten los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="1e482-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e482-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e482-116">Return value</span></span>

<span data-ttu-id="1e482-117">Si envía este mensaje explícitamente, devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1e482-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e482-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e482-118">Remarks</span></span>

<span data-ttu-id="1e482-119">El valor de estado de un elemento incluye un conjunto de marcadores de bits que indican el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="1e482-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="1e482-120">El valor de estado también puede incluir índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición.</span><span class="sxs-lookup"><span data-stu-id="1e482-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e482-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e482-121">Requirements</span></span>



| <span data-ttu-id="1e482-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e482-122">Requirement</span></span> | <span data-ttu-id="1e482-123">Value</span><span class="sxs-lookup"><span data-stu-id="1e482-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e482-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e482-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e482-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1e482-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e482-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e482-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e482-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e482-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e482-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e482-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e482-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e482-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





