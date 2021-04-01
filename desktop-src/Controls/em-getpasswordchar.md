---
title: Mensaje de EM_GETPASSWORDCHAR (Winuser. h)
description: Obtiene el carácter de la contraseña que muestra un control de edición cuando el usuario escribe texto. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905525"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="5ea2e-105">\_Mensaje GETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="5ea2e-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="5ea2e-106">Obtiene el carácter de la contraseña que muestra un control de edición cuando el usuario escribe texto.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="5ea2e-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ea2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea2e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ea2e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea2e-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ea2e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ea2e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea2e-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea2e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea2e-113">Return value</span></span>

<span data-ttu-id="5ea2e-114">El valor devuelto especifica el carácter que se va a mostrar en lugar de los caracteres que escriba el usuario.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="5ea2e-115">Si el valor devuelto es **null**, no hay ningún carácter de contraseña y el control muestra los caracteres que escribe el usuario.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea2e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea2e-116">Remarks</span></span>

<span data-ttu-id="5ea2e-117">Si se crea un control de edición con el estilo de [**\_ contraseña de es**](edit-control-styles.md) , el carácter de contraseña predeterminado se establece en un asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="5ea2e-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="5ea2e-118">Si se crea un control de edición sin el estilo de **\_ contraseña** es, no hay ningún carácter de contraseña.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="5ea2e-119">Para cambiar el carácter de contraseña, envíe el mensaje [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="5ea2e-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="5ea2e-120">**Controles de edición:** Los controles de edición multilínea no admiten el estilo de contraseña ni los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="5ea2e-121">**Edición enriquecida:** Compatible con Microsoft Rich Edit 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="5ea2e-122">Los controles de edición de línea única y multilínea admiten el estilo de contraseña y los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5ea2e-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="5ea2e-123">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="5ea2e-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea2e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea2e-124">Requirements</span></span>



| <span data-ttu-id="5ea2e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea2e-125">Requirement</span></span> | <span data-ttu-id="5ea2e-126">Value</span><span class="sxs-lookup"><span data-stu-id="5ea2e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea2e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea2e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea2e-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ea2e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ea2e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea2e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea2e-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ea2e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ea2e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea2e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea2e-132"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea2e-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea2e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea2e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea2e-134">**\_SETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="5ea2e-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 





