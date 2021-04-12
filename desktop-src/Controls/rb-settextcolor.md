---
title: Mensaje de RB_SETTEXTCOLOR (commctrl. h)
description: Establece el color de texto predeterminado del control rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491752"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="8d8e1-104">Mensaje de SETTEXTCOLOR de RB \_</span><span class="sxs-lookup"><span data-stu-id="8d8e1-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="8d8e1-105">Establece el color de texto predeterminado del control rebar.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d8e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d8e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d8e1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d8e1-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d8e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d8e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8e1-110">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de texto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8e1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d8e1-111">Return value</span></span>

<span data-ttu-id="8d8e1-112">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de texto predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8e1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d8e1-113">Remarks</span></span>

<span data-ttu-id="8d8e1-114">El color de texto predeterminado del control rebar se usa para dibujar el texto en un control rebar y se han enviado todas las bandas que se agregan después de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8d8e1-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="8d8e1-115">El color de texto predeterminado para una banda determinada se puede invalidar Cuando se agrega o se modifica una banda mediante la configuración de la \_ marca de colores RBBIM en **fMask** y el establecimiento de **ClrBack** en la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8d8e1-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d8e1-116">Requirements</span></span>



| <span data-ttu-id="8d8e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d8e1-117">Requirement</span></span> | <span data-ttu-id="8d8e1-118">Value</span><span class="sxs-lookup"><span data-stu-id="8d8e1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8e1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d8e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8e1-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d8e1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d8e1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d8e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8e1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d8e1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d8e1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d8e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8e1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d8e1-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8e1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d8e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8e1-126">**\_GETTEXTCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="8d8e1-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

