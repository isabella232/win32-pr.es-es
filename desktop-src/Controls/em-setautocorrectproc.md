---
title: Mensaje EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Define el procedimiento de devolución de llamada de Autocorrección actual.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- EM_SETAUTOCORRECTPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492484"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="27014-104">\_Mensaje SETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="27014-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="27014-105">Define el procedimiento de devolución de llamada de Autocorrección actual.</span><span class="sxs-lookup"><span data-stu-id="27014-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="27014-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27014-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27014-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27014-108">La función de devolución de llamada [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="27014-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="27014-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27014-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27014-110">No se utiliza; debe ser cero</span><span class="sxs-lookup"><span data-stu-id="27014-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27014-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27014-111">Return value</span></span>

<span data-ttu-id="27014-112">Si la operación se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="27014-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="27014-113">Si se produce un error en la operación, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="27014-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="27014-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27014-114">Requirements</span></span>



| <span data-ttu-id="27014-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="27014-115">Requirement</span></span> | <span data-ttu-id="27014-116">Value</span><span class="sxs-lookup"><span data-stu-id="27014-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27014-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27014-117">Minimum supported client</span></span><br/> | <span data-ttu-id="27014-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="27014-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="27014-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27014-119">Minimum supported server</span></span><br/> | <span data-ttu-id="27014-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="27014-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27014-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27014-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="27014-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27014-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27014-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="27014-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27014-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="27014-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="27014-125">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="27014-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="27014-126">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="27014-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





