---
title: Mensaje de EM_SETPASSWORDCHAR (Winuser. h)
description: Establece o quita el carácter de contraseña de un control de edición. Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490228"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="031ac-106">\_Mensaje SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="031ac-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="031ac-107">Establece o quita el carácter de contraseña de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="031ac-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="031ac-108">Cuando se establece un carácter de contraseña, ese carácter se muestra en lugar de los caracteres que escribe el usuario.</span><span class="sxs-lookup"><span data-stu-id="031ac-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="031ac-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="031ac-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="031ac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="031ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031ac-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="031ac-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="031ac-112">Carácter que se va a mostrar en lugar de los caracteres especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="031ac-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="031ac-113">Si este parámetro es cero, el control quita el carácter de contraseña actual y muestra los caracteres que escribe el usuario.</span><span class="sxs-lookup"><span data-stu-id="031ac-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="031ac-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="031ac-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="031ac-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="031ac-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031ac-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="031ac-116">Return value</span></span>

<span data-ttu-id="031ac-117">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="031ac-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="031ac-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="031ac-118">Remarks</span></span>

<span data-ttu-id="031ac-119">Cuando un control de edición recibe el mensaje **\_ SETPASSWORDCHAR em** , el control vuelve a dibujar todos los caracteres visibles mediante el carácter especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="031ac-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="031ac-120">Si *wParam* es cero, el control vuelve a dibujar todos los caracteres visibles con los caracteres que escribe el usuario.</span><span class="sxs-lookup"><span data-stu-id="031ac-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="031ac-121">Si se crea un control de edición con el estilo de [**\_ contraseña de es**](edit-control-styles.md) , el carácter de contraseña predeterminado se establece en un asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="031ac-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="031ac-122">Si se crea un control de edición sin el estilo de **\_ contraseña** es, no hay ningún carácter de contraseña.</span><span class="sxs-lookup"><span data-stu-id="031ac-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="031ac-123">Se quita el estilo de **\_ contraseña** de es si se envía un mensaje **\_ SETPASSWORDCHAR em** con el parámetro *wParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="031ac-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="031ac-124">**Controles de edición:** Los controles de edición multilínea no admiten el estilo de contraseña ni los mensajes.</span><span class="sxs-lookup"><span data-stu-id="031ac-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="031ac-125">**Edición enriquecida:** Compatible con Microsoft Rich Edit 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="031ac-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="031ac-126">Los controles de edición de línea única y multilínea admiten el estilo de contraseña y los mensajes.</span><span class="sxs-lookup"><span data-stu-id="031ac-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="031ac-127">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="031ac-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="031ac-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="031ac-128">Requirements</span></span>



| <span data-ttu-id="031ac-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="031ac-129">Requirement</span></span> | <span data-ttu-id="031ac-130">Value</span><span class="sxs-lookup"><span data-stu-id="031ac-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="031ac-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="031ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="031ac-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="031ac-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="031ac-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="031ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="031ac-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="031ac-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="031ac-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="031ac-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="031ac-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="031ac-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="031ac-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="031ac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031ac-138">**\_GETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="031ac-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 





