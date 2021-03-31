---
title: Mensaje EM_GETTEXTEX (RichEdit. h)
description: Obtiene el texto de un control Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490372"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="3d31d-104">\_Mensaje GETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="3d31d-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="3d31d-105">Obtiene el texto de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3d31d-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d31d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d31d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d31d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d31d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d31d-108">Puntero a una estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , que indica cómo traducir el texto antes de colocarlo en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="3d31d-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3d31d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d31d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d31d-110">Puntero al búfer para recibir el texto.</span><span class="sxs-lookup"><span data-stu-id="3d31d-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="3d31d-111">El miembro **CB** de la estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) especifica el tamaño de este búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3d31d-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="3d31d-112">Use el [**mensaje \_ GETTEXTLENGTHEX em**](em-gettextlengthex.md) para obtener el tamaño necesario del búfer.</span><span class="sxs-lookup"><span data-stu-id="3d31d-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d31d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d31d-113">Return value</span></span>

<span data-ttu-id="3d31d-114">El valor devuelto es el número de elementos **TCHAR** copiados en el búfer de salida, incluido el terminador null.</span><span class="sxs-lookup"><span data-stu-id="3d31d-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d31d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d31d-115">Remarks</span></span>

<span data-ttu-id="3d31d-116">Si el tamaño del búfer de salida es menor que el tamaño del texto del control, el control de edición copiará el texto desde el principio y lo colocará en el búfer hasta que el búfer esté lleno.</span><span class="sxs-lookup"><span data-stu-id="3d31d-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="3d31d-117">Un carácter nulo de terminación se seguirá colocando al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="3d31d-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="3d31d-118">Si se solicita texto ANSI, **em \_ GETTEXTEX** utiliza la función [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para convertir los caracteres Unicode a ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d31d-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="3d31d-119">Permite pasar de Unicode a ANSI mediante una página de códigos determinada.</span><span class="sxs-lookup"><span data-stu-id="3d31d-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="3d31d-120">La estructura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contiene miembros (**lpDefaultChar** y **lpUsedDefChar**) que se usan en la traducción de Unicode a ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d31d-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d31d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d31d-121">Requirements</span></span>



| <span data-ttu-id="3d31d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d31d-122">Requirement</span></span> | <span data-ttu-id="3d31d-123">Value</span><span class="sxs-lookup"><span data-stu-id="3d31d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d31d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d31d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d31d-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3d31d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d31d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d31d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d31d-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d31d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d31d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d31d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d31d-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d31d-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d31d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d31d-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d31d-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3d31d-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3d31d-132">**\_SETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="3d31d-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="3d31d-133">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="3d31d-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="3d31d-134">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="3d31d-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3d31d-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="3d31d-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="3d31d-136">**SETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3d31d-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

