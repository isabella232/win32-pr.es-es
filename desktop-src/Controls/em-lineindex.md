---
title: Mensaje de EM_LINEINDEX (Winuser. h)
description: Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_LINEINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996225"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="1d1f3-104">Mensaje de EM_LINEINDEX (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="1d1f3-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="1d1f3-105">Obtiene el índice de carácter del primer carácter de una línea especificada en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="1d1f3-106">Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="1d1f3-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d1f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d1f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d1f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d1f3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d1f3-110">Número de línea de base cero.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-110">The zero-based line number.</span></span> <span data-ttu-id="1d1f3-111">Un valor de-1 especifica el número de línea actual (la línea que contiene el símbolo de intercalación).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="1d1f3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d1f3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d1f3-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d1f3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d1f3-114">Return value</span></span>

<span data-ttu-id="1d1f3-115">El valor devuelto es el índice de carácter de la línea especificada en el parámetro *wParam* o es-1 si el número de línea especificado es mayor que el número de líneas del control de edición.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d1f3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d1f3-116">Remarks</span></span>

<span data-ttu-id="1d1f3-117">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1d1f3-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1d1f3-118">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f3-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1f3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d1f3-119">Requirements</span></span>



| <span data-ttu-id="1d1f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1f3-120">Requirement</span></span> | <span data-ttu-id="1d1f3-121">Value</span><span class="sxs-lookup"><span data-stu-id="1d1f3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1f3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d1f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1f3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1d1f3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d1f3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d1f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1f3-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d1f3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d1f3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d1f3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d1f3-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d1f3-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d1f3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d1f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d1f3-129">**\_LINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="1d1f3-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 





