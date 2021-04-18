---
title: Mensaje EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Llama a la función de devolución de llamada de Autocorrección almacenada por el \_ mensaje em SETAUTOCORRECTPROC, siempre que el texto que precede al punto de inserción sea un candidato para la corrección automática.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491518"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="67335-104">\_Mensaje CALLAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="67335-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="67335-105">Llama a la función de devolución de llamada de Autocorrección almacenada por el mensaje [**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , siempre que el texto que precede al punto de inserción sea un candidato para la corrección automática.</span><span class="sxs-lookup"><span data-stu-id="67335-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="67335-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67335-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67335-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67335-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67335-108">Carácter de tipo **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="67335-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="67335-109">Si este carácter es una tabulación (U + 0009) y el carácter que precede al punto de inserción no es una tabulación, el carácter que precede al punto de inserción se trata como parte de la cadena candidata de Autocorrección en lugar de como un delimitador de cadena. de lo contrario, *wParam* no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="67335-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="67335-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67335-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67335-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="67335-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67335-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67335-112">Return value</span></span>

<span data-ttu-id="67335-113">El valor devuelto es cero si el mensaje se realiza correctamente, o es distinto de cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="67335-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="67335-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67335-114">Requirements</span></span>



| <span data-ttu-id="67335-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="67335-115">Requirement</span></span> | <span data-ttu-id="67335-116">Value</span><span class="sxs-lookup"><span data-stu-id="67335-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67335-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67335-117">Minimum supported client</span></span><br/> | <span data-ttu-id="67335-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="67335-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="67335-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67335-119">Minimum supported server</span></span><br/> | <span data-ttu-id="67335-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="67335-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67335-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67335-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="67335-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67335-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67335-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="67335-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67335-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="67335-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="67335-125">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="67335-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="67335-126">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="67335-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





