---
title: Mensaje EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcula la longitud del texto de varias maneras. Normalmente se llama a antes de crear un búfer para recibir el texto del control.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905198"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="03386-105">\_Mensaje GETTEXTLENGTHEX em</span><span class="sxs-lookup"><span data-stu-id="03386-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="03386-106">Calcula la longitud del texto de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="03386-106">Calculates text length in various ways.</span></span> <span data-ttu-id="03386-107">Normalmente se llama a antes de crear un búfer para recibir el texto del control.</span><span class="sxs-lookup"><span data-stu-id="03386-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="03386-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03386-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03386-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03386-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03386-110">Puntero a una estructura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) que recibe la información de longitud del texto.</span><span class="sxs-lookup"><span data-stu-id="03386-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="03386-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03386-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03386-112">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="03386-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03386-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03386-113">Return value</span></span>

<span data-ttu-id="03386-114">El mensaje devuelve el número de **TCHAR** en el control de edición, dependiendo de la configuración de las marcas de la estructura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) .</span><span class="sxs-lookup"><span data-stu-id="03386-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="03386-115">Si se establecieron marcas incompatibles en el miembro **Flags** , el mensaje devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="03386-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="03386-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03386-116">Remarks</span></span>

<span data-ttu-id="03386-117">Este mensaje es una manera rápida y sencilla de determinar el número de caracteres de la versión Unicode del control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="03386-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="03386-118">Sin embargo, en el caso de una página de códigos de destino no Unicode, se convertirá en una combinación de caracteres de un solo byte y de doble byte.</span><span class="sxs-lookup"><span data-stu-id="03386-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="03386-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03386-119">Requirements</span></span>



| <span data-ttu-id="03386-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="03386-120">Requirement</span></span> | <span data-ttu-id="03386-121">Value</span><span class="sxs-lookup"><span data-stu-id="03386-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03386-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03386-122">Minimum supported client</span></span><br/> | <span data-ttu-id="03386-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="03386-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03386-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03386-124">Minimum supported server</span></span><br/> | <span data-ttu-id="03386-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="03386-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03386-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03386-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="03386-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="03386-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03386-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="03386-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03386-129">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="03386-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





