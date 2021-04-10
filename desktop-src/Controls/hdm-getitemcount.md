---
title: Mensaje de HDM_GETITEMCOUNT (commctrl. h)
description: Obtiene un recuento de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150554"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="ae439-105">HDM \_ GETITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="ae439-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="ae439-106">Obtiene un recuento de los elementos de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ae439-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="ae439-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="ae439-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae439-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae439-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae439-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae439-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ae439-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ae439-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ae439-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae439-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae439-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ae439-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae439-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae439-113">Return value</span></span>

<span data-ttu-id="ae439-114">Devuelve el número de elementos si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ae439-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae439-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae439-115">Requirements</span></span>



| <span data-ttu-id="ae439-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae439-116">Requirement</span></span> | <span data-ttu-id="ae439-117">Value</span><span class="sxs-lookup"><span data-stu-id="ae439-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae439-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae439-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae439-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ae439-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae439-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae439-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae439-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae439-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae439-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae439-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae439-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae439-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





