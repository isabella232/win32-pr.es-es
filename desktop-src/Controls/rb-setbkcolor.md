---
title: Mensaje de RB_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo predeterminado del control rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658227"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="76395-104">Mensaje de SETBKCOLOR de RB \_</span><span class="sxs-lookup"><span data-stu-id="76395-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="76395-105">Establece el color de fondo predeterminado del control rebar.</span><span class="sxs-lookup"><span data-stu-id="76395-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="76395-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76395-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76395-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76395-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="76395-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76395-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76395-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76395-110">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de fondo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="76395-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76395-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76395-111">Return value</span></span>

<span data-ttu-id="76395-112">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="76395-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="76395-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76395-113">Remarks</span></span>

<span data-ttu-id="76395-114">El color de fondo predeterminado del control rebar se usa para dibujar el fondo en un control rebar y se han enviado todas las bandas que se agregan después de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="76395-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="76395-115">El color de fondo predeterminado para una banda determinada se puede invalidar Cuando se agrega o se modifica una banda mediante la configuración de la \_ marca de colores RBBIM en **fMask** y el establecimiento de **ClrBack** en la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="76395-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="76395-116">Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="76395-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="76395-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76395-117">Requirements</span></span>



| <span data-ttu-id="76395-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76395-118">Requirement</span></span> | <span data-ttu-id="76395-119">Value</span><span class="sxs-lookup"><span data-stu-id="76395-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76395-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76395-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76395-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76395-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76395-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76395-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76395-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="76395-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76395-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76395-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76395-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76395-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76395-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="76395-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76395-127">**\_GETBKCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="76395-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

