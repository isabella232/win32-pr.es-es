---
title: Mensaje EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Obtiene un puntero a la función AutoCorrectProc definida por la aplicación.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491008"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="61c2b-104">\_Mensaje GETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="61c2b-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="61c2b-105">Obtiene un puntero a la función [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="61c2b-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="61c2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c2b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61c2b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61c2b-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="61c2b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="61c2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61c2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61c2b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="61c2b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c2b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c2b-111">Return value</span></span>

<span data-ttu-id="61c2b-112">Devuelve un puntero a la función [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="61c2b-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c2b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c2b-113">Requirements</span></span>



| <span data-ttu-id="61c2b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c2b-114">Requirement</span></span> | <span data-ttu-id="61c2b-115">Value</span><span class="sxs-lookup"><span data-stu-id="61c2b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61c2b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61c2b-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="61c2b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61c2b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61c2b-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="61c2b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61c2b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61c2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61c2b-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="61c2b-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c2b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="61c2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c2b-123">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="61c2b-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="61c2b-124">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="61c2b-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="61c2b-125">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="61c2b-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





