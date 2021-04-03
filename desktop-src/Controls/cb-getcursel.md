---
title: Mensaje de CB_GETCURSEL (Winuser. h)
description: Una aplicación envía un \_ mensaje CB GETCURSEL para recuperar el índice del elemento seleccionado actualmente, si existe, en el cuadro de lista de un cuadro combinado.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905707"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="1d006-104">\_Mensaje GETCURSEL CB</span><span class="sxs-lookup"><span data-stu-id="1d006-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="1d006-105">Una aplicación envía un mensaje **CB \_ GETCURSEL** para recuperar el índice del elemento seleccionado actualmente, si existe, en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="1d006-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d006-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d006-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d006-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d006-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1d006-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1d006-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d006-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d006-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1d006-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d006-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d006-111">Return value</span></span>

<span data-ttu-id="1d006-112">El valor devuelto es el índice de base cero del elemento actualmente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1d006-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="1d006-113">Si no hay ningún elemento seleccionado, se trata de un \_ error CB.</span><span class="sxs-lookup"><span data-stu-id="1d006-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d006-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d006-114">Requirements</span></span>



| <span data-ttu-id="1d006-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d006-115">Requirement</span></span> | <span data-ttu-id="1d006-116">Value</span><span class="sxs-lookup"><span data-stu-id="1d006-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d006-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d006-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d006-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1d006-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d006-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d006-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d006-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d006-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d006-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d006-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d006-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d006-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d006-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d006-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d006-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1d006-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d006-125">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="1d006-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="1d006-126">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="1d006-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





