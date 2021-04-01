---
title: Mensaje de CB_RESETCONTENT (Winuser. h)
description: Quita todos los elementos del cuadro de lista y el control de edición de un cuadro combinado.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905240"
---
# <a name="cb_resetcontent-message"></a><span data-ttu-id="dced7-104">\_Mensaje RESETCONTENT CB</span><span class="sxs-lookup"><span data-stu-id="dced7-104">CB\_RESETCONTENT message</span></span>

<span data-ttu-id="dced7-105">Quita todos los elementos del cuadro de lista y el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="dced7-105">Removes all items from the list box and edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="dced7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dced7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dced7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dced7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dced7-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dced7-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dced7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dced7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dced7-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dced7-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dced7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dced7-111">Return value</span></span>

<span data-ttu-id="dced7-112">Este mensaje siempre devuelve CB \_ bien.</span><span class="sxs-lookup"><span data-stu-id="dced7-112">This message always returns CB\_OKAY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dced7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dced7-113">Remarks</span></span>

<span data-ttu-id="dced7-114">Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el propietario del cuadro combinado recibirá un mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) para cada elemento del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="dced7-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the owner of the combo box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="dced7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dced7-115">Requirements</span></span>



| <span data-ttu-id="dced7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dced7-116">Requirement</span></span> | <span data-ttu-id="dced7-117">Value</span><span class="sxs-lookup"><span data-stu-id="dced7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dced7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dced7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dced7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dced7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dced7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dced7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dced7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dced7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dced7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dced7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dced7-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dced7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dced7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dced7-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="dced7-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dced7-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dced7-126">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="dced7-126">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="dced7-127">**WM \_ DELETEITEM**</span><span class="sxs-lookup"><span data-stu-id="dced7-127">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





