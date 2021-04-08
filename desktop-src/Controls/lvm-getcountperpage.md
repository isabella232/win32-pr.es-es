---
title: Mensaje de LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcula el número de elementos que pueden ajustarse verticalmente en el área visible de un control de vista de lista cuando está en la vista de lista o de informe. Solo se cuentan los elementos totalmente visibles. Puede enviar este mensaje explícitamente o mediante la \_ macro GetCountPerPage de ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078870"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="a669b-106">\_Mensaje GETCOUNTPERPAGE LVM</span><span class="sxs-lookup"><span data-stu-id="a669b-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="a669b-107">Calcula el número de elementos que pueden ajustarse verticalmente en el área visible de un control de vista de lista cuando está en la vista de lista o de informe.</span><span class="sxs-lookup"><span data-stu-id="a669b-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="a669b-108">Solo se cuentan los elementos totalmente visibles.</span><span class="sxs-lookup"><span data-stu-id="a669b-108">Only fully visible items are counted.</span></span> <span data-ttu-id="a669b-109">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetCountPerPage de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .</span><span class="sxs-lookup"><span data-stu-id="a669b-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a669b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a669b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a669b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a669b-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a669b-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a669b-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a669b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a669b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a669b-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a669b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a669b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a669b-115">Return value</span></span>

<span data-ttu-id="a669b-116">Devuelve el número de elementos totalmente visibles si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a669b-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="a669b-117">Si la vista actual es un icono o una vista de iconos pequeños, el valor devuelto es el número total de elementos del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="a669b-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a669b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a669b-118">Requirements</span></span>



| <span data-ttu-id="a669b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a669b-119">Requirement</span></span> | <span data-ttu-id="a669b-120">Value</span><span class="sxs-lookup"><span data-stu-id="a669b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a669b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a669b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a669b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a669b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a669b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a669b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a669b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a669b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a669b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a669b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a669b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a669b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





