---
title: Mensaje de LB_GETHORIZONTALEXTENT (Winuser. h)
description: Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997030"
---
# <a name="lb_gethorizontalextent-message"></a><span data-ttu-id="bde56-104">\_Mensaje lb GETHORIZONTALEXTENT</span><span class="sxs-lookup"><span data-stu-id="bde56-104">LB\_GETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="bde56-105">Obtiene el ancho, en píxeles, que un cuadro de lista se puede desplazar horizontalmente (el ancho desplazable) si el cuadro de lista tiene una barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="bde56-105">Gets the width, in pixels, that a list box can be scrolled horizontally (the scrollable width) if the list box has a horizontal scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bde56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bde56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde56-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bde56-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde56-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bde56-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bde56-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bde56-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bde56-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bde56-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde56-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bde56-111">Return value</span></span>

<span data-ttu-id="bde56-112">El valor devuelto es el ancho desplazable, en píxeles, del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="bde56-112">The return value is the scrollable width, in pixels, of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="bde56-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bde56-113">Remarks</span></span>

<span data-ttu-id="bde56-114">Para responder al mensaje de **lb \_ GETHORIZONTALEXTENT** , el cuadro de lista se debe haber definido con el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="bde56-114">To respond to the **LB\_GETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="bde56-115">Si la aplicación no establece la extensión horizontal del cuadro de lista (con [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), la extensión horizontal predeterminada es cero.</span><span class="sxs-lookup"><span data-stu-id="bde56-115">If the application does not set the horizontal extent of the list box (using [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), the default horizontal extent is zero.</span></span> <span data-ttu-id="bde56-116">Tenga en cuenta que el cuadro de lista no actualiza dinámicamente su extensión horizontal.</span><span class="sxs-lookup"><span data-stu-id="bde56-116">Note that the list box does not update its horizontal extent dynamically.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde56-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bde56-117">Requirements</span></span>



| <span data-ttu-id="bde56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde56-118">Requirement</span></span> | <span data-ttu-id="bde56-119">Value</span><span class="sxs-lookup"><span data-stu-id="bde56-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde56-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bde56-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bde56-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bde56-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bde56-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bde56-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bde56-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bde56-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bde56-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bde56-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde56-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bde56-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde56-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bde56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde56-127">**LB \_ SETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="bde56-127">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

