---
title: Mensaje EM_SETELLIPSISMODE (RichEdit. h)
description: Este mensaje establece el modo de puntos suspensivos actual.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079662"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="57eb3-104">\_Mensaje SETELLIPSISMODE em</span><span class="sxs-lookup"><span data-stu-id="57eb3-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="57eb3-105">Este mensaje establece el modo de puntos suspensivos actual.</span><span class="sxs-lookup"><span data-stu-id="57eb3-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="57eb3-106">Cuando está habilitada, se muestra un botón de puntos suspensivos () para el texto que no cabe en la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="57eb3-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="57eb3-107">Los puntos suspensivos solo se usan cuando el control no está activo.</span><span class="sxs-lookup"><span data-stu-id="57eb3-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="57eb3-108">Cuando está activo, las barras de desplazamiento se utilizan para mostrar el texto que no cabe en la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="57eb3-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="57eb3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57eb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57eb3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57eb3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57eb3-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="57eb3-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57eb3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57eb3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57eb3-113">DWORD que recibe uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="57eb3-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="57eb3-114">Value</span><span class="sxs-lookup"><span data-stu-id="57eb3-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="57eb3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="57eb3-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="57eb3-116"><dt>**puntos suspensivos \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="57eb3-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="57eb3-117">No se usa ningún botón de puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="57eb3-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="57eb3-118"><dt>**fin de los puntos suspensivos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="57eb3-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="57eb3-119">Puntos suspensivos al final (interrupción forzada).</span><span class="sxs-lookup"><span data-stu-id="57eb3-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="57eb3-120"><dt>**Palabra de puntos suspensivos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="57eb3-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="57eb3-121">Puntos suspensivos al final (salto de palabra).</span><span class="sxs-lookup"><span data-stu-id="57eb3-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="57eb3-122">Los bits de estos valores caben en la **\_ máscara de puntos suspensivos**.</span><span class="sxs-lookup"><span data-stu-id="57eb3-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57eb3-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57eb3-123">Return value</span></span>

<span data-ttu-id="57eb3-124">Si wParam es 0 y lParam es uno de los valores de la tabla anterior, el valor devuelto es igual a TRUE. de lo contrario, el valor devuelto es igual a FALSE.</span><span class="sxs-lookup"><span data-stu-id="57eb3-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="57eb3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57eb3-125">Requirements</span></span>



| <span data-ttu-id="57eb3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="57eb3-126">Requirement</span></span> | <span data-ttu-id="57eb3-127">Value</span><span class="sxs-lookup"><span data-stu-id="57eb3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57eb3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57eb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="57eb3-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="57eb3-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="57eb3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57eb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="57eb3-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="57eb3-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57eb3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57eb3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="57eb3-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57eb3-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57eb3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="57eb3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57eb3-135">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="57eb3-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="57eb3-136">**\_GETELLIPSISSTATE em**</span><span class="sxs-lookup"><span data-stu-id="57eb3-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





