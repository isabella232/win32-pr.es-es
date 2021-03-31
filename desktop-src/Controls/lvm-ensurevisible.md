---
title: Mensaje de LVM_ENSUREVISIBLE (commctrl. h)
description: Garantiza que un elemento de vista de lista es totalmente o parcialmente visible, desplazando el control de vista de lista si es necesario. Puede enviar este mensaje explícitamente o mediante la \_ macro ensureVisible de ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995941"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="22301-105">\_Mensaje ENSUREVISIBLE de LVM</span><span class="sxs-lookup"><span data-stu-id="22301-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="22301-106">Garantiza que un elemento de vista de lista es totalmente o parcialmente visible, desplazando el control de vista de lista si es necesario.</span><span class="sxs-lookup"><span data-stu-id="22301-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="22301-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ ensureVisible de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="22301-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="22301-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22301-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22301-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22301-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="22301-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="22301-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22301-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22301-112">Valor que especifica si el elemento debe estar totalmente visible.</span><span class="sxs-lookup"><span data-stu-id="22301-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="22301-113">Si este parámetro es **true**, no se produce ningún desplazamiento si el elemento está al menos parcialmente visible.</span><span class="sxs-lookup"><span data-stu-id="22301-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22301-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22301-114">Return value</span></span>

<span data-ttu-id="22301-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="22301-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="22301-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22301-116">Remarks</span></span>

<span data-ttu-id="22301-117">Se produce un error en el mensaje si el estilo de ventana incluye [**LVS \_ noscroll**](list-view-window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="22301-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22301-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22301-118">Requirements</span></span>



| <span data-ttu-id="22301-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22301-119">Requirement</span></span> | <span data-ttu-id="22301-120">Value</span><span class="sxs-lookup"><span data-stu-id="22301-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22301-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22301-121">Minimum supported client</span></span><br/> | <span data-ttu-id="22301-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22301-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22301-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22301-123">Minimum supported server</span></span><br/> | <span data-ttu-id="22301-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22301-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22301-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22301-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="22301-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22301-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





