---
title: Mensaje de LVM_UPDATE (commctrl. h)
description: Actualiza un elemento de vista de lista. Si el control de vista de lista tiene el \_ estilo LVS AutoArrange, esta macro hace que el control de vista de lista esté organizado. Puede enviar este mensaje explícitamente o mediante la macro de \_ actualización de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905030"
---
# <a name="lvm_update-message"></a><span data-ttu-id="6365f-106">Mensaje de actualización de LVM \_</span><span class="sxs-lookup"><span data-stu-id="6365f-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="6365f-107">Actualiza un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="6365f-107">Updates a list-view item.</span></span> <span data-ttu-id="6365f-108">Si el control de vista de lista tiene el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) , esta macro hace que el control de vista de lista esté organizado.</span><span class="sxs-lookup"><span data-stu-id="6365f-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="6365f-109">Puede enviar este mensaje explícitamente o mediante la macro [**de \_ actualización de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .</span><span class="sxs-lookup"><span data-stu-id="6365f-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6365f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6365f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6365f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6365f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6365f-112">Índice del elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="6365f-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="6365f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6365f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6365f-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6365f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6365f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6365f-115">Return value</span></span>

<span data-ttu-id="6365f-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6365f-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6365f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6365f-117">Requirements</span></span>



| <span data-ttu-id="6365f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6365f-118">Requirement</span></span> | <span data-ttu-id="6365f-119">Value</span><span class="sxs-lookup"><span data-stu-id="6365f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6365f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6365f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6365f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6365f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6365f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6365f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6365f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6365f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6365f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6365f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6365f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6365f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





