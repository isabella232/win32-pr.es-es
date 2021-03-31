---
title: Mensaje EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera el estado de los puntos suspensivos actuales.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- EM_GETELLIPSISSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490726"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="fc426-104">\_Mensaje GETELLIPSISSTATE em</span><span class="sxs-lookup"><span data-stu-id="fc426-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="fc426-105">Recupera el estado de los puntos suspensivos actuales.</span><span class="sxs-lookup"><span data-stu-id="fc426-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="fc426-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc426-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc426-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc426-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fc426-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc426-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc426-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc426-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fc426-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc426-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc426-111">Return value</span></span>

<span data-ttu-id="fc426-112">El valor devuelto es TRUE si se muestran puntos suspensivos y FALSE en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fc426-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc426-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc426-113">Requirements</span></span>



| <span data-ttu-id="fc426-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc426-114">Requirement</span></span> | <span data-ttu-id="fc426-115">Value</span><span class="sxs-lookup"><span data-stu-id="fc426-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc426-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc426-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc426-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc426-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fc426-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc426-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc426-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc426-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc426-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc426-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc426-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc426-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc426-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc426-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc426-123">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="fc426-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="fc426-124">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="fc426-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





