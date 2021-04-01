---
title: Mensaje de LVM_SETHOVERTIME (commctrl. h)
description: Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetHoverTime de ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149896"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="77c4f-105">\_Mensaje SETHOVERTIME LVM</span><span class="sxs-lookup"><span data-stu-id="77c4f-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="77c4f-106">Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione.</span><span class="sxs-lookup"><span data-stu-id="77c4f-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="77c4f-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetHoverTime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .</span><span class="sxs-lookup"><span data-stu-id="77c4f-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77c4f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77c4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77c4f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77c4f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="77c4f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77c4f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77c4f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77c4f-112">La nueva cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione.</span><span class="sxs-lookup"><span data-stu-id="77c4f-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="77c4f-113">Si este valor es (**DWORD**)-1, el tiempo de desplazamiento se establece en el tiempo de desplazamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="77c4f-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c4f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77c4f-114">Return value</span></span>

<span data-ttu-id="77c4f-115">Devuelve el tiempo de desplazamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="77c4f-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c4f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77c4f-116">Remarks</span></span>

<span data-ttu-id="77c4f-117">El tiempo de desplazamiento solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77c4f-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c4f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77c4f-118">Requirements</span></span>



| <span data-ttu-id="77c4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77c4f-119">Requirement</span></span> | <span data-ttu-id="77c4f-120">Value</span><span class="sxs-lookup"><span data-stu-id="77c4f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77c4f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77c4f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77c4f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="77c4f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77c4f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77c4f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77c4f-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="77c4f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77c4f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77c4f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77c4f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77c4f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





