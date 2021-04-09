---
title: Mensaje de CB_GETDROPPEDSTATE (Winuser. h)
description: Determina si el cuadro de lista de un cuadro combinado está desplegado.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079786"
---
# <a name="cb_getdroppedstate-message"></a><span data-ttu-id="edbe9-104">\_Mensaje GETDROPPEDSTATE CB</span><span class="sxs-lookup"><span data-stu-id="edbe9-104">CB\_GETDROPPEDSTATE message</span></span>

<span data-ttu-id="edbe9-105">Determina si el cuadro de lista de un cuadro combinado está desplegado.</span><span class="sxs-lookup"><span data-stu-id="edbe9-105">Determines whether the list box of a combo box is dropped down.</span></span>

## <a name="parameters"></a><span data-ttu-id="edbe9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbe9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edbe9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edbe9-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edbe9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="edbe9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edbe9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edbe9-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edbe9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edbe9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbe9-111">Return value</span></span>

<span data-ttu-id="edbe9-112">Si el cuadro de lista está visible, el valor devuelto es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="edbe9-112">If the list box is visible, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbe9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edbe9-113">Requirements</span></span>



| <span data-ttu-id="edbe9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbe9-114">Requirement</span></span> | <span data-ttu-id="edbe9-115">Value</span><span class="sxs-lookup"><span data-stu-id="edbe9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbe9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbe9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="edbe9-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edbe9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="edbe9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbe9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="edbe9-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="edbe9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="edbe9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edbe9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbe9-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edbe9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbe9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="edbe9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbe9-123">**CB \_ SHOWDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="edbe9-123">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)
</dt> </dl>

 

 





