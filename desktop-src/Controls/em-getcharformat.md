---
title: Mensaje EM_GETCHARFORMAT (RichEdit. h)
description: Determina el formato de caracteres en un control Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079456"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="2cc87-104">\_Mensaje GETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="2cc87-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="2cc87-105">Determina el formato de caracteres en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2cc87-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cc87-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cc87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cc87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc87-108">Especifica el intervalo de texto del que se va a recuperar el formato.</span><span class="sxs-lookup"><span data-stu-id="2cc87-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="2cc87-109">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2cc87-109">It can be one of the following values.</span></span>



| <span data-ttu-id="2cc87-110">Value</span><span class="sxs-lookup"><span data-stu-id="2cc87-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="2cc87-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2cc87-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="2cc87-112"><dt>**\_valor predeterminado de SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2cc87-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="2cc87-113">El formato de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2cc87-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="2cc87-114"><dt>**selección de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cc87-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="2cc87-115">Formato de caracteres de la selección actual.</span><span class="sxs-lookup"><span data-stu-id="2cc87-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc87-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cc87-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc87-117">Estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) que recibe los atributos del primer carácter.</span><span class="sxs-lookup"><span data-stu-id="2cc87-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="2cc87-118">El miembro **dwMask** especifica qué atributos son coherentes en toda la selección.</span><span class="sxs-lookup"><span data-stu-id="2cc87-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="2cc87-119">Por ejemplo, si toda la selección está en cursiva o no en cursiva, \_ se establece cfm cursiva; si la selección está en parte en cursiva y no en parte, cfm \_ cursiva no se establece.</span><span class="sxs-lookup"><span data-stu-id="2cc87-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="2cc87-120">Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que es una extensión de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="2cc87-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="2cc87-121">Antes de enviar el mensaje **\_ GETCHARFORMAT em** , establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="2cc87-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc87-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cc87-122">Return value</span></span>

<span data-ttu-id="2cc87-123">Este mensaje devuelve el valor del miembro **dwMask** de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="2cc87-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc87-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cc87-124">Requirements</span></span>



| <span data-ttu-id="2cc87-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc87-125">Requirement</span></span> | <span data-ttu-id="2cc87-126">Value</span><span class="sxs-lookup"><span data-stu-id="2cc87-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc87-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cc87-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc87-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2cc87-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2cc87-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cc87-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc87-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cc87-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2cc87-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cc87-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc87-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc87-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc87-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cc87-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="2cc87-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2cc87-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2cc87-135">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2cc87-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="2cc87-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="2cc87-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





