---
title: Mensaje de EM_GETENDOFLINE (commctrl. h)
description: Recupera el carácter de final de línea utilizado cuando se inserta un LineBreak. Envíe este mensaje explícitamente o mediante la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489466"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="2f674-105">\_Mensaje GETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="2f674-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="2f674-106">Recupera el carácter de fin de línea para un control de edición.</span><span class="sxs-lookup"><span data-stu-id="2f674-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="2f674-107">Envíe este mensaje explícitamente o mediante la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .</span><span class="sxs-lookup"><span data-stu-id="2f674-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f674-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f674-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f674-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f674-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f674-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f674-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f674-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f674-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f674-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f674-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f674-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f674-113">Return value</span></span>

<span data-ttu-id="2f674-114">Devuelve el carácter de final de línea utilizado por el control de edición.</span><span class="sxs-lookup"><span data-stu-id="2f674-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="2f674-115">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f674-115">This can be one of the following values.</span></span>

| <span data-ttu-id="2f674-116">Value</span><span class="sxs-lookup"><span data-stu-id="2f674-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="2f674-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2f674-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="2f674-118"><dt>**\_CRLF ENDOFLINE \_ EC**</dt></span><span class="sxs-lookup"><span data-stu-id="2f674-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="2f674-119">El carácter de final de línea usado para New saltos es el retorno de carro seguido de avance de línea (CRLF).</span><span class="sxs-lookup"><span data-stu-id="2f674-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="2f674-120"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="2f674-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="2f674-121">El carácter de final de línea usado para New saltos es el retorno de carro (CR).</span><span class="sxs-lookup"><span data-stu-id="2f674-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="2f674-122"><dt>**\_ENDOFLINE de \_ LF de EC**</dt></span><span class="sxs-lookup"><span data-stu-id="2f674-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="2f674-123">El carácter de final de línea usado para New saltos es avance de línea (LF).</span><span class="sxs-lookup"><span data-stu-id="2f674-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="2f674-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f674-124">Remarks</span></span>

<span data-ttu-id="2f674-125">Cuando el carácter de final de línea usado se establece en **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** con [**Editar \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), este mensaje devolverá el carácter de final de línea detectado.</span><span class="sxs-lookup"><span data-stu-id="2f674-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f674-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f674-126">Requirements</span></span>



| <span data-ttu-id="2f674-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f674-127">Requirement</span></span> | <span data-ttu-id="2f674-128">Value</span><span class="sxs-lookup"><span data-stu-id="2f674-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f674-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f674-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f674-130">Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f674-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f674-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f674-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f674-132">Solo aplicaciones de escritorio de Windows Server 2019 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f674-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f674-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f674-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f674-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f674-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f674-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f674-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f674-136">\**\_SETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="2f674-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





