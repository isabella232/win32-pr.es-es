---
title: Mensaje de LVM_SETHOTITEM (commctrl. h)
description: Establece el elemento activo para un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetHotItem de ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801106"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="c9166-105">\_Mensaje SETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="c9166-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="c9166-106">Establece el elemento activo para un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="c9166-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="c9166-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetHotItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .</span><span class="sxs-lookup"><span data-stu-id="c9166-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9166-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9166-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9166-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9166-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9166-110">Índice de base cero del elemento que se va a establecer como elemento activo.</span><span class="sxs-lookup"><span data-stu-id="c9166-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="c9166-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9166-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c9166-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c9166-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9166-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9166-113">Return value</span></span>

<span data-ttu-id="c9166-114">Devuelve el índice del elemento que antes estaba activo.</span><span class="sxs-lookup"><span data-stu-id="c9166-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9166-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9166-115">Requirements</span></span>



| <span data-ttu-id="c9166-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9166-116">Requirement</span></span> | <span data-ttu-id="c9166-117">Value</span><span class="sxs-lookup"><span data-stu-id="c9166-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9166-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9166-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9166-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9166-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9166-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9166-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9166-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9166-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9166-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9166-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9166-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9166-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





