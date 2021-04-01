---
title: Mensaje EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera el texto de composición del editor de métodos de entrada (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996749"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="4acdd-104">\_Mensaje GETIMECOMPTEXT em</span><span class="sxs-lookup"><span data-stu-id="4acdd-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="4acdd-105">Recupera el texto de composición del editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="4acdd-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="4acdd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4acdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4acdd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4acdd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4acdd-108">Estructura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .</span><span class="sxs-lookup"><span data-stu-id="4acdd-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4acdd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4acdd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4acdd-110">Búfer que recibe el texto de la composición.</span><span class="sxs-lookup"><span data-stu-id="4acdd-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="4acdd-111">El tamaño de este búfer está incluido en el miembro **CB** de la estructura *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4acdd-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4acdd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4acdd-112">Return value</span></span>

<span data-ttu-id="4acdd-113">Si se realiza correctamente, el valor devuelto es el número de caracteres Unicode copiados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4acdd-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="4acdd-114">De lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="4acdd-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4acdd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4acdd-115">Remarks</span></span>

<span data-ttu-id="4acdd-116">Este mensaje solo toma cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="4acdd-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="4acdd-117">**Advertencia de seguridad:** Asegúrese de tener un búfer suficiente para el tamaño de la entrada.</span><span class="sxs-lookup"><span data-stu-id="4acdd-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="4acdd-118">Si no lo hace, podrían producirse problemas en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4acdd-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="4acdd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4acdd-119">Requirements</span></span>



| <span data-ttu-id="4acdd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4acdd-120">Requirement</span></span> | <span data-ttu-id="4acdd-121">Value</span><span class="sxs-lookup"><span data-stu-id="4acdd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4acdd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4acdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4acdd-123">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="4acdd-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4acdd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4acdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4acdd-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4acdd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4acdd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4acdd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4acdd-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4acdd-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4acdd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4acdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4acdd-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="4acdd-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





