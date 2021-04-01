---
title: Mensaje EM_GETPARAFORMAT (RichEdit. h)
description: Recupera el formato de párrafo de la selección actual en un control Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996929"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="3b665-104">\_Mensaje GETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="3b665-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="3b665-105">Recupera el formato de párrafo de la selección actual en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3b665-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b665-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b665-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b665-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b665-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3b665-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3b665-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b665-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b665-110">Puntero a una estructura de [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recibe los atributos de formato de párrafo de la selección actual.</span><span class="sxs-lookup"><span data-stu-id="3b665-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="3b665-111">Si se selecciona más de un párrafo, la estructura recibe los atributos del primer párrafo y el miembro **dwMask** especifica qué atributos son coherentes en toda la selección.</span><span class="sxs-lookup"><span data-stu-id="3b665-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="3b665-112">Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que es una extensión de la estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="3b665-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="3b665-113">Antes de enviar el mensaje **\_ GETPARAFORMAT em** , establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="3b665-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b665-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b665-114">Return value</span></span>

<span data-ttu-id="3b665-115">Este mensaje devuelve el valor del miembro **dwMask** de la estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="3b665-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b665-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b665-116">Requirements</span></span>



| <span data-ttu-id="3b665-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b665-117">Requirement</span></span> | <span data-ttu-id="3b665-118">Value</span><span class="sxs-lookup"><span data-stu-id="3b665-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b665-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b665-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b665-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b665-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b665-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b665-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b665-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b665-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b665-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b665-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b665-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b665-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b665-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b665-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b665-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3b665-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b665-127">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3b665-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="3b665-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="3b665-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





