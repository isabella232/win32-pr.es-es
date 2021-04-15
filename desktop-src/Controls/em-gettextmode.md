---
title: Mensaje EM_GETTEXTMODE (RichEdit. h)
description: Obtiene el nivel de texto actual y el nivel de deshacer de un control Rich Edit.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- EM_GETTEXTMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492005"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="bc37d-104">\_Mensaje GETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="bc37d-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="bc37d-105">Obtiene el nivel de texto actual y el nivel de deshacer de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bc37d-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc37d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc37d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc37d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc37d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc37d-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc37d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc37d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc37d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc37d-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc37d-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc37d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc37d-111">Return value</span></span>

<span data-ttu-id="bc37d-112">El valor devuelto es uno o más valores del tipo de enumeración [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="bc37d-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="bc37d-113">Los valores indican el modo de texto actual y el nivel de deshacer del control.</span><span class="sxs-lookup"><span data-stu-id="bc37d-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc37d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc37d-114">Requirements</span></span>



| <span data-ttu-id="bc37d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc37d-115">Requirement</span></span> | <span data-ttu-id="bc37d-116">Value</span><span class="sxs-lookup"><span data-stu-id="bc37d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc37d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc37d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bc37d-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc37d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc37d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc37d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bc37d-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc37d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc37d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc37d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc37d-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc37d-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc37d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc37d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc37d-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bc37d-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc37d-125">**\_SETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="bc37d-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="bc37d-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="bc37d-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





