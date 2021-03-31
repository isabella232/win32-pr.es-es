---
title: Mensaje de EM_LINEFROMCHAR (Winuser. h)
description: Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150140"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="56004-104">\_Mensaje LINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="56004-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="56004-105">Obtiene el índice de la línea que contiene el índice de carácter especificado en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="56004-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="56004-106">Un índice de carácter es el índice de base cero del carácter desde el principio del control de edición.</span><span class="sxs-lookup"><span data-stu-id="56004-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="56004-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="56004-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="56004-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56004-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56004-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56004-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56004-110">Índice de carácter del carácter incluido en la línea cuyo número se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="56004-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="56004-111">Si este parámetro es-1, **em \_ LINEFROMCHAR** recupera el número de línea de la línea actual (la línea que contiene el símbolo de intercalación) o, si hay una selección, el número de línea de la línea que contiene el principio de la selección.</span><span class="sxs-lookup"><span data-stu-id="56004-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="56004-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56004-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56004-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="56004-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56004-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56004-114">Return value</span></span>

<span data-ttu-id="56004-115">El valor devuelto es el número de línea de base cero de la línea que contiene el índice de caracteres especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="56004-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="56004-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56004-116">Remarks</span></span>

<span data-ttu-id="56004-117">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="56004-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="56004-118">Si el índice de caracteres es mayor que 64.000, use el mensaje [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="56004-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="56004-119">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="56004-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56004-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56004-120">Requirements</span></span>



| <span data-ttu-id="56004-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="56004-121">Requirement</span></span> | <span data-ttu-id="56004-122">Value</span><span class="sxs-lookup"><span data-stu-id="56004-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56004-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56004-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56004-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56004-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56004-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56004-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56004-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56004-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56004-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56004-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56004-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56004-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56004-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="56004-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="56004-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="56004-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56004-131">**\_EXLINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="56004-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="56004-132">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="56004-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





