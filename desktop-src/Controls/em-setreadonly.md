---
title: Mensaje de EM_SETREADONLY (Winuser. h)
description: Establece o quita el estilo de solo lectura (ES \_ ReadOnly) de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150230"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="49973-105">\_Mensaje SETREADONLY em</span><span class="sxs-lookup"><span data-stu-id="49973-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="49973-106">Establece o quita el estilo de solo lectura ([**es \_ ReadOnly**](edit-control-styles.md)) de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="49973-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="49973-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="49973-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="49973-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49973-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49973-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49973-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49973-110">Especifica si se debe establecer o quitar el estilo [**es de \_ solo lectura**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="49973-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="49973-111">Un valor de **true** establece el estilo **es de \_ solo lectura** ; un valor de **false** quita el estilo **es de \_ solo lectura** .</span><span class="sxs-lookup"><span data-stu-id="49973-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="49973-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49973-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49973-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="49973-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49973-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49973-114">Return value</span></span>

<span data-ttu-id="49973-115">Si la operación se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="49973-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="49973-116">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="49973-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="49973-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49973-117">Remarks</span></span>

<span data-ttu-id="49973-118">Cuando un control de edición tiene el estilo [**es de \_ solo lectura**](edit-control-styles.md) , el usuario no puede cambiar el texto dentro del control de edición.</span><span class="sxs-lookup"><span data-stu-id="49973-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="49973-119">Para determinar si un control de edición tiene el estilo [**es de \_ solo lectura**](edit-control-styles.md) , use la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con la \_ marca de estilo GWL.</span><span class="sxs-lookup"><span data-stu-id="49973-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="49973-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="49973-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="49973-121">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="49973-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49973-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49973-122">Requirements</span></span>



| <span data-ttu-id="49973-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49973-123">Requirement</span></span> | <span data-ttu-id="49973-124">Value</span><span class="sxs-lookup"><span data-stu-id="49973-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49973-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49973-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49973-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49973-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49973-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49973-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49973-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="49973-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49973-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49973-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="49973-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49973-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49973-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="49973-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49973-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="49973-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

