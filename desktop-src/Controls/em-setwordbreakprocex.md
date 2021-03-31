---
title: Mensaje EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Establece el procedimiento extendido de separación de palabras para un control Rich Edit.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- EM_SETWORDBREAKPROCEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996222"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="b67b5-104">\_Mensaje SETWORDBREAKPROCEX em</span><span class="sxs-lookup"><span data-stu-id="b67b5-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="b67b5-105">Establece el procedimiento extendido de separación de palabras para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b67b5-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b67b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b67b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b67b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b67b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b67b5-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b67b5-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b67b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b67b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b67b5-110">Puntero a una función [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) o **null** para usar el procedimiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b67b5-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b67b5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b67b5-111">Return value</span></span>

<span data-ttu-id="b67b5-112">Este mensaje devuelve la dirección del procedimiento extendido de separación de palabras anterior.</span><span class="sxs-lookup"><span data-stu-id="b67b5-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b67b5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b67b5-113">Requirements</span></span>



| <span data-ttu-id="b67b5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b67b5-114">Requirement</span></span> | <span data-ttu-id="b67b5-115">Value</span><span class="sxs-lookup"><span data-stu-id="b67b5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b67b5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b67b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b67b5-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b67b5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b67b5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b67b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b67b5-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b67b5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b67b5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b67b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67b5-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67b5-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b67b5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b67b5-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="b67b5-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b67b5-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b67b5-124">**EditWordBreakProcEx**</span><span class="sxs-lookup"><span data-stu-id="b67b5-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="b67b5-125">**\_GETWORDBREAKPROCEX em**</span><span class="sxs-lookup"><span data-stu-id="b67b5-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





