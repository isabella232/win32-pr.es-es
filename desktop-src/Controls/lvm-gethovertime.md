---
title: Mensaje de LVM_GETHOVERTIME (commctrl. h)
description: Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHoverTime de ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491465"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="86db6-105">\_Mensaje GETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="86db6-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="86db6-106">Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione.</span><span class="sxs-lookup"><span data-stu-id="86db6-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="86db6-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHoverTime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .</span><span class="sxs-lookup"><span data-stu-id="86db6-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="86db6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86db6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86db6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="86db6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="86db6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="86db6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86db6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86db6-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="86db6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86db6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86db6-113">Return value</span></span>

<span data-ttu-id="86db6-114">Devuelve la cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione.</span><span class="sxs-lookup"><span data-stu-id="86db6-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="86db6-115">Si el valor devuelto es (**DWORD**)-1, el tiempo de activación es el tiempo de desplazamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="86db6-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="86db6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86db6-116">Remarks</span></span>

<span data-ttu-id="86db6-117">El tiempo de desplazamiento solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="86db6-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="86db6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86db6-118">Requirements</span></span>



| <span data-ttu-id="86db6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86db6-119">Requirement</span></span> | <span data-ttu-id="86db6-120">Value</span><span class="sxs-lookup"><span data-stu-id="86db6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86db6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86db6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86db6-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86db6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86db6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86db6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86db6-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="86db6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86db6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86db6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86db6-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86db6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





