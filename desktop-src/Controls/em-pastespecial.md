---
title: Mensaje EM_PASTESPECIAL (RichEdit. h)
description: Pega un formato específico del portapapeles en un control Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905366"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="cb795-104">\_Mensaje PASTESPECIAL em</span><span class="sxs-lookup"><span data-stu-id="cb795-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="cb795-105">Pega un formato específico del portapapeles en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cb795-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb795-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb795-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb795-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb795-108">Especifica los [formatos del portapapeles](/windows/desktop/dataxchg/clipboard-formats).</span><span class="sxs-lookup"><span data-stu-id="cb795-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="cb795-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb795-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb795-110">Puntero a una estructura [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) o **null**.</span><span class="sxs-lookup"><span data-stu-id="cb795-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="cb795-111">Si se pega un objeto, la estructura **REPASTESPECIAL** se rellena con el aspecto deseado.</span><span class="sxs-lookup"><span data-stu-id="cb795-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="cb795-112">Si *lParam* es **null** o el miembro **dwAspect** es cero, el aspecto de presentación utilizado será el contenido del descriptor de objeto.</span><span class="sxs-lookup"><span data-stu-id="cb795-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb795-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb795-113">Return value</span></span>

<span data-ttu-id="cb795-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cb795-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb795-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb795-115">Requirements</span></span>



| <span data-ttu-id="cb795-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb795-116">Requirement</span></span> | <span data-ttu-id="cb795-117">Value</span><span class="sxs-lookup"><span data-stu-id="cb795-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb795-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb795-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb795-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb795-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb795-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb795-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb795-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb795-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb795-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb795-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb795-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb795-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb795-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb795-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb795-125">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="cb795-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

