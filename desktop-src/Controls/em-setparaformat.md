---
title: Mensaje EM_SETPARAFORMAT (RichEdit. h)
description: Establece el formato de párrafo para la selección actual en un control Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490229"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="74ceb-104">\_Mensaje SETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="74ceb-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="74ceb-105">Establece el formato de párrafo para la selección actual en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="74ceb-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="74ceb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74ceb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ceb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74ceb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ceb-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="74ceb-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74ceb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74ceb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ceb-110">Puntero a una estructura de [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que especifica los nuevos atributos de formato de párrafo.</span><span class="sxs-lookup"><span data-stu-id="74ceb-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="74ceb-111">Solo se cambian los atributos especificados por el miembro **dwMask** .</span><span class="sxs-lookup"><span data-stu-id="74ceb-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="74ceb-112">Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que es una extensión de la estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="74ceb-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="74ceb-113">Antes de enviar el mensaje **\_ SETPARAFORMAT em** , establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="74ceb-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ceb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74ceb-114">Return value</span></span>

<span data-ttu-id="74ceb-115">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="74ceb-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="74ceb-116">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="74ceb-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ceb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ceb-117">Requirements</span></span>



| <span data-ttu-id="74ceb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ceb-118">Requirement</span></span> | <span data-ttu-id="74ceb-119">Value</span><span class="sxs-lookup"><span data-stu-id="74ceb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74ceb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ceb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74ceb-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="74ceb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74ceb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ceb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74ceb-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74ceb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74ceb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74ceb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ceb-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ceb-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ceb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="74ceb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="74ceb-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="74ceb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74ceb-128">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="74ceb-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="74ceb-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="74ceb-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





