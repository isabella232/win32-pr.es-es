---
title: Mensaje EM_GETIMECOLOR (RichEdit. h)
description: Recupera el color de composición del editor de métodos de entrada (IME).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996750"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="5369a-104">\_Mensaje GETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="5369a-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="5369a-105">Recupera el color de composición del editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="5369a-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="5369a-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="5369a-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="5369a-107">No se admite en las versiones posteriores de Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5369a-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="5369a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5369a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5369a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5369a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5369a-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5369a-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5369a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5369a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5369a-112">Matriz de cuatro elementos de estructuras [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que recibe el color de la composición.</span><span class="sxs-lookup"><span data-stu-id="5369a-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5369a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5369a-113">Return value</span></span>

<span data-ttu-id="5369a-114">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5369a-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5369a-115">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="5369a-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5369a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5369a-116">Requirements</span></span>



| <span data-ttu-id="5369a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5369a-117">Requirement</span></span> | <span data-ttu-id="5369a-118">Value</span><span class="sxs-lookup"><span data-stu-id="5369a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5369a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5369a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5369a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5369a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5369a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5369a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5369a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5369a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5369a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5369a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5369a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5369a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5369a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5369a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5369a-126">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5369a-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





