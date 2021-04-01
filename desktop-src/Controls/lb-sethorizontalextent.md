---
title: Mensaje de LB_SETHORIZONTALEXTENT (Winuser. h)
description: Establece el ancho, en píxeles, por el que se puede desplazar un cuadro de lista horizontalmente (el ancho desplazable).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905513"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="ea9a2-104">\_Mensaje lb SETHORIZONTALEXTENT</span><span class="sxs-lookup"><span data-stu-id="ea9a2-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="ea9a2-105">Establece el ancho, en píxeles, por el que se puede desplazar un cuadro de lista horizontalmente (el ancho desplazable).</span><span class="sxs-lookup"><span data-stu-id="ea9a2-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="ea9a2-106">Si el ancho del cuadro de lista es menor que este valor, la barra de desplazamiento horizontal se desplaza horizontalmente por los elementos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="ea9a2-107">Si el ancho del cuadro de lista es igual o mayor que este valor, se oculta la barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea9a2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea9a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea9a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9a2-110">Especifica el número de píxeles que se puede desplazar el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="ea9a2-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="ea9a2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea9a2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9a2-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9a2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea9a2-114">Return value</span></span>

<span data-ttu-id="ea9a2-115">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9a2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea9a2-116">Remarks</span></span>

<span data-ttu-id="ea9a2-117">Para responder al mensaje de **lb \_ SETHORIZONTALEXTENT** , el cuadro de lista se debe haber definido con el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="ea9a2-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="ea9a2-118">Tenga en cuenta que un cuadro de lista no actualiza dinámicamente su extensión horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="ea9a2-119">Este mensaje no tiene ningún efecto en un cuadro de lista de varias columnas.</span><span class="sxs-lookup"><span data-stu-id="ea9a2-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9a2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea9a2-120">Requirements</span></span>



| <span data-ttu-id="ea9a2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea9a2-121">Requirement</span></span> | <span data-ttu-id="ea9a2-122">Value</span><span class="sxs-lookup"><span data-stu-id="ea9a2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9a2-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea9a2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9a2-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea9a2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea9a2-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea9a2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9a2-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea9a2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea9a2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea9a2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9a2-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea9a2-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9a2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea9a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9a2-130">**LB \_ GETHORIZONTALEXTENT**</span><span class="sxs-lookup"><span data-stu-id="ea9a2-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

