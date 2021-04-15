---
title: Mensaje de EM_GETFILELINE (CommCtrl. h)
description: Copia una línea de texto de un control de edición, independientemente de cómo se muestran las líneas en la pantalla y la coloca en un búfer especificado.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491812"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="aa550-104">Mensaje de EM_GETFILELINE (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="aa550-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="aa550-105">Copia una línea de texto de un control de edición, independientemente de cómo se muestran las líneas en la pantalla y la coloca en un búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="aa550-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa550-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa550-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa550-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa550-108">Índice de base cero de la línea que se va a recuperar de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="aa550-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="aa550-109">Un valor de cero especifica la línea superior.</span><span class="sxs-lookup"><span data-stu-id="aa550-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="aa550-110">Este parámetro se omite en un control de edición de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="aa550-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="aa550-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa550-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa550-112">Puntero al búfer que recibe una copia de la línea.</span><span class="sxs-lookup"><span data-stu-id="aa550-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="aa550-113">Antes de enviar el mensaje, establezca la primera palabra de este búfer en el tamaño, en **TCHAR** s, del búfer.</span><span class="sxs-lookup"><span data-stu-id="aa550-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="aa550-114">Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aa550-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="aa550-115">La línea copiada sobrescribe el tamaño de la primera palabra.</span><span class="sxs-lookup"><span data-stu-id="aa550-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa550-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa550-116">Return value</span></span>

<span data-ttu-id="aa550-117">El valor devuelto es el número **de elementos** que se han copiado.</span><span class="sxs-lookup"><span data-stu-id="aa550-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="aa550-118">El valor devuelto es cero si el número de línea especificado por el parámetro *wParam* es mayor que el número de líneas en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="aa550-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa550-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa550-119">Remarks</span></span>

<span data-ttu-id="aa550-120">La línea copiada no contiene un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="aa550-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa550-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa550-121">Requirements</span></span>



| <span data-ttu-id="aa550-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa550-122">Requirement</span></span> | <span data-ttu-id="aa550-123">Value</span><span class="sxs-lookup"><span data-stu-id="aa550-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa550-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa550-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa550-125">Solo aplicaciones de escritorio de Windows 10 y 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa550-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa550-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa550-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa550-127">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa550-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa550-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa550-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa550-129"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa550-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa550-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa550-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa550-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="aa550-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa550-132">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="aa550-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="aa550-133">**Editar \_ GetFileLine**</span><span class="sxs-lookup"><span data-stu-id="aa550-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="aa550-134">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="aa550-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aa550-135">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="aa550-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

