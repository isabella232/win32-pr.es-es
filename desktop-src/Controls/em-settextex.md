---
title: Mensaje EM_SETTEXTEX (RichEdit. h)
description: Combina la funcionalidad de los mensajes de WM \_ SETTEXT y em \_ REPLACESEL, y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491201"
---
# <a name="em_settextex-message"></a><span data-ttu-id="4aeaf-104">\_Mensaje SETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="4aeaf-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="4aeaf-105">Combina la funcionalidad de los mensajes de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) y [**em \_ REPLACESEL**](em-replacesel.md) , y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="4aeaf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4aeaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aeaf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4aeaf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aeaf-108">Puntero a una estructura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica las marcas y una página de códigos opcional que se va a usar para traducir a Unicode.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="4aeaf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4aeaf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4aeaf-110">Puntero al texto terminado en null que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="4aeaf-111">Este texto es una cadena ANSI, a menos que la página de códigos sea 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="4aeaf-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="4aeaf-112">Si *lParam* comienza con una secuencia ASCII RTF válida, por ejemplo, "{ \\ rtf" o "{urtf", el texto se lee mediante el lector RTF.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aeaf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aeaf-113">Return value</span></span>

<span data-ttu-id="4aeaf-114">Si la operación está estableciendo todo el texto y se realiza correctamente, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="4aeaf-115">Si la operación está estableciendo la selección y se realiza correctamente, el valor devuelto es el número de bytes o caracteres copiados.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="4aeaf-116">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aeaf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aeaf-117">Requirements</span></span>



| <span data-ttu-id="4aeaf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aeaf-118">Requirement</span></span> | <span data-ttu-id="4aeaf-119">Value</span><span class="sxs-lookup"><span data-stu-id="4aeaf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aeaf-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4aeaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4aeaf-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4aeaf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4aeaf-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4aeaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4aeaf-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4aeaf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4aeaf-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4aeaf-124">Redistributable</span></span><br/>          | <span data-ttu-id="4aeaf-125">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="4aeaf-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="4aeaf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4aeaf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aeaf-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aeaf-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aeaf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aeaf-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aeaf-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4aeaf-130">**\_GETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="4aeaf-131">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

