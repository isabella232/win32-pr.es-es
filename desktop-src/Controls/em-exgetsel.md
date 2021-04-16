---
title: Mensaje EM_EXGETSEL (RichEdit. h)
description: Recupera las posiciones de caracteres inicial y final de la selección en un control Rich Edit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- EM_EXGETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491488"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="447c8-104">\_Mensaje EXGETSEL em</span><span class="sxs-lookup"><span data-stu-id="447c8-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="447c8-105">Recupera las posiciones de caracteres inicial y final de la selección en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="447c8-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="447c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="447c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="447c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="447c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="447c8-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="447c8-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="447c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="447c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="447c8-110">Una estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que recibe el intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="447c8-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="447c8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="447c8-111">Return value</span></span>

<span data-ttu-id="447c8-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="447c8-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="447c8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="447c8-113">Requirements</span></span>



| <span data-ttu-id="447c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="447c8-114">Requirement</span></span> | <span data-ttu-id="447c8-115">Value</span><span class="sxs-lookup"><span data-stu-id="447c8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="447c8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="447c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="447c8-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="447c8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="447c8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="447c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="447c8-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="447c8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="447c8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="447c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="447c8-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="447c8-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="447c8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="447c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447c8-123">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="447c8-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





