---
title: Mensaje de CB_SETEDITSEL (Winuser. h)
description: Una aplicación envía un \_ mensaje CB SETEDITSEL para seleccionar caracteres en el control de edición de un cuadro combinado.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490523"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="cfca2-104">\_Mensaje SETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="cfca2-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="cfca2-105">Una aplicación envía un mensaje **CB \_ SETEDITSEL** para seleccionar caracteres en el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cfca2-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfca2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfca2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfca2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfca2-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cfca2-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cfca2-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfca2-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfca2-110">El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="cfca2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="cfca2-111">Si el **LOWORD** es-1, la selección, si la hay, se quita.</span><span class="sxs-lookup"><span data-stu-id="cfca2-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="cfca2-112">El [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* especifica la posición final.</span><span class="sxs-lookup"><span data-stu-id="cfca2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="cfca2-113">Si el **HIWORD** es-1, se selecciona todo el texto desde la posición inicial hasta el último carácter del control de edición.</span><span class="sxs-lookup"><span data-stu-id="cfca2-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfca2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfca2-114">Return value</span></span>

<span data-ttu-id="cfca2-115">Si el mensaje se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="cfca2-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="cfca2-116">Si el mensaje se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="cfca2-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfca2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfca2-117">Remarks</span></span>

<span data-ttu-id="cfca2-118">Las posiciones son de base cero.</span><span class="sxs-lookup"><span data-stu-id="cfca2-118">The positions are zero-based.</span></span> <span data-ttu-id="cfca2-119">El primer carácter del control de edición se encuentra en la posición cero.</span><span class="sxs-lookup"><span data-stu-id="cfca2-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="cfca2-120">El primer carácter que está después del último carácter seleccionado se encuentra en la posición final.</span><span class="sxs-lookup"><span data-stu-id="cfca2-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="cfca2-121">Por ejemplo, para seleccionar los cuatro primeros caracteres del control de edición, utilice una posición inicial de 0 y una posición final de 4.</span><span class="sxs-lookup"><span data-stu-id="cfca2-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfca2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfca2-122">Requirements</span></span>



| <span data-ttu-id="cfca2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfca2-123">Requirement</span></span> | <span data-ttu-id="cfca2-124">Value</span><span class="sxs-lookup"><span data-stu-id="cfca2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfca2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfca2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfca2-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cfca2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfca2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfca2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfca2-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfca2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfca2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfca2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfca2-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfca2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfca2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfca2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfca2-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cfca2-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfca2-133">**CB \_ GETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="cfca2-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="cfca2-134">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="cfca2-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cfca2-135">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="cfca2-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

