---
title: Mensaje EM_SETBKGNDCOLOR (RichEdit. h)
description: El \_ mensaje SETBKGNDCOLOR em establece el color de fondo de un control Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905524"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="b65d1-104">\_Mensaje SETBKGNDCOLOR em</span><span class="sxs-lookup"><span data-stu-id="b65d1-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="b65d1-105">El **mensaje \_ SETBKGNDCOLOR em** establece el color de fondo de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b65d1-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b65d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b65d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b65d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b65d1-108">Especifica si se va a utilizar el color del sistema.</span><span class="sxs-lookup"><span data-stu-id="b65d1-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="b65d1-109">Si este parámetro es un valor distinto de cero, el fondo se establece en el color del sistema de fondo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b65d1-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="b65d1-110">De lo contrario, el fondo se establece en el color especificado.</span><span class="sxs-lookup"><span data-stu-id="b65d1-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="b65d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b65d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b65d1-112">Estructura [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el color si *wParam* es cero.</span><span class="sxs-lookup"><span data-stu-id="b65d1-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="b65d1-113">Para generar un **COLORREF**, use la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="b65d1-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65d1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b65d1-114">Return value</span></span>

<span data-ttu-id="b65d1-115">Este mensaje devuelve el color de fondo original.</span><span class="sxs-lookup"><span data-stu-id="b65d1-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65d1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b65d1-116">Requirements</span></span>



| <span data-ttu-id="b65d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65d1-117">Requirement</span></span> | <span data-ttu-id="b65d1-118">Value</span><span class="sxs-lookup"><span data-stu-id="b65d1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b65d1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b65d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b65d1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b65d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b65d1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b65d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b65d1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b65d1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b65d1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b65d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b65d1-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b65d1-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65d1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b65d1-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b65d1-126">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="b65d1-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b65d1-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="b65d1-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="b65d1-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="b65d1-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

