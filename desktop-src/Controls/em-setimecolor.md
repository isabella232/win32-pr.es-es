---
title: Mensaje EM_SETIMECOLOR (RichEdit. h)
description: Establece el color de composición del editor de métodos de entrada (IME) para un control Rich Edit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491213"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="9c8cf-104">\_Mensaje SETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="9c8cf-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="9c8cf-105">Establece el color de composición del editor de métodos de entrada (IME) para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="9c8cf-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="9c8cf-107">No se admite en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="9c8cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c8cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c8cf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8cf-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c8cf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c8cf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c8cf-112">Puntero a una estructura [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que contiene el color de composición que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8cf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c8cf-113">Return value</span></span>

<span data-ttu-id="9c8cf-114">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9c8cf-115">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c8cf-116">Requirements</span></span>



| <span data-ttu-id="9c8cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c8cf-117">Requirement</span></span> | <span data-ttu-id="9c8cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="9c8cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8cf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c8cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8cf-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c8cf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c8cf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c8cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8cf-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c8cf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c8cf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c8cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c8cf-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c8cf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c8cf-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c8cf-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="9c8cf-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c8cf-127">**\_GETIMECOLOR em**</span><span class="sxs-lookup"><span data-stu-id="9c8cf-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="9c8cf-128">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9c8cf-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





