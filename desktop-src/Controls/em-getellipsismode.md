---
title: Mensaje EM_GETELLIPSISMODE (RichEdit. h)
description: Recupera el modo de puntos suspensivos actual.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150321"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="7f3a1-104">\_Mensaje GETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="7f3a1-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="7f3a1-105">Recupera el modo de puntos suspensivos actual.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="7f3a1-106">Cuando está habilitada, se muestra un botón de puntos suspensivos () para el texto que no cabe en la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="7f3a1-107">Los puntos suspensivos solo se usan cuando el control no está activo.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="7f3a1-108">Cuando está activo, las barras de desplazamiento se utilizan para mostrar el texto que no cabe en la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="7f3a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f3a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3a1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f3a1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3a1-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f3a1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f3a1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3a1-113">Puntero a un valor DWORD que recibe uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="7f3a1-114">Value</span><span class="sxs-lookup"><span data-stu-id="7f3a1-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7f3a1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7f3a1-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="7f3a1-116"><dt>**puntos suspensivos \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a1-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="7f3a1-117">No se usa ningún botón de puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="7f3a1-118"><dt>**fin de los puntos suspensivos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a1-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="7f3a1-119">Puntos suspensivos al final (interrupción forzada).</span><span class="sxs-lookup"><span data-stu-id="7f3a1-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="7f3a1-120"><dt>**Palabra de puntos suspensivos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a1-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="7f3a1-121">Puntos suspensivos al final (salto de palabra).</span><span class="sxs-lookup"><span data-stu-id="7f3a1-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3a1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f3a1-122">Return value</span></span>

<span data-ttu-id="7f3a1-123">Si wParam es 0 y lParam no es NULL, el valor devuelto es igual a TRUE; de lo contrario, el valor devuelto es igual a FALSE.</span><span class="sxs-lookup"><span data-stu-id="7f3a1-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f3a1-124">Requirements</span></span>



| <span data-ttu-id="7f3a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3a1-125">Requirement</span></span> | <span data-ttu-id="7f3a1-126">Value</span><span class="sxs-lookup"><span data-stu-id="7f3a1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3a1-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3a1-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3a1-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7f3a1-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f3a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3a1-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f3a1-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f3a1-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f3a1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3a1-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f3a1-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3a1-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f3a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3a1-134">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="7f3a1-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="7f3a1-135">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="7f3a1-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





