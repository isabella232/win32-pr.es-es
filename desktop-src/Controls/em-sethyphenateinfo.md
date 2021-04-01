---
title: Mensaje EM_SETHYPHENATEINFO (RichEdit. h)
description: Establece la forma en que un control Rich Edit realiza la división en guiones.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905522"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="2a349-104">\_Mensaje SETHYPHENATEINFO em</span><span class="sxs-lookup"><span data-stu-id="2a349-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="2a349-105">Establece la forma en que un control Rich Edit realiza la división en guiones.</span><span class="sxs-lookup"><span data-stu-id="2a349-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a349-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a349-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a349-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a349-108">Puntero a una estructura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="2a349-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2a349-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a349-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a349-110">No se utiliza, debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2a349-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a349-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a349-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2a349-112">Para habilitar la división de palabras, el cliente debe llamar a [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), especificando a \_ ADVANCEDTYPOGRAPHY.</span><span class="sxs-lookup"><span data-stu-id="2a349-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a349-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a349-113">Requirements</span></span>



| <span data-ttu-id="2a349-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a349-114">Requirement</span></span> | <span data-ttu-id="2a349-115">Value</span><span class="sxs-lookup"><span data-stu-id="2a349-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a349-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a349-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a349-117">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a349-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a349-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a349-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a349-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a349-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a349-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a349-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a349-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a349-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a349-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a349-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a349-123">**\_GETHYPHENATEINFO em**</span><span class="sxs-lookup"><span data-stu-id="2a349-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





