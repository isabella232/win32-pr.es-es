---
title: Mensaje de LB_SETCARETINDEX (Winuser. h)
description: Establece el rectángulo de foco en el elemento en el índice especificado de un cuadro de lista de selección múltiple. Si el elemento no está visible, se desplaza a la vista.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905514"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="85aef-105">\_Mensaje lb SETCARETINDEX</span><span class="sxs-lookup"><span data-stu-id="85aef-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="85aef-106">Establece el rectángulo de foco en el elemento en el índice especificado de un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="85aef-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="85aef-107">Si el elemento no está visible, se desplaza a la vista.</span><span class="sxs-lookup"><span data-stu-id="85aef-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="85aef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85aef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85aef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85aef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85aef-110">Especifica el índice de base cero del elemento de cuadro de lista que va a recibir el rectángulo de foco.</span><span class="sxs-lookup"><span data-stu-id="85aef-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="85aef-111">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="85aef-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="85aef-112">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="85aef-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="85aef-113">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="85aef-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="85aef-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85aef-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85aef-115">Si este valor es **false**, el elemento se desplaza hasta que esté totalmente visible; Si es **true**, el elemento se desplaza hasta que esté al menos parcialmente visible.</span><span class="sxs-lookup"><span data-stu-id="85aef-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85aef-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85aef-116">Return value</span></span>

<span data-ttu-id="85aef-117">Si se produce un error, el valor devuelto es LB \_ Err (-1).</span><span class="sxs-lookup"><span data-stu-id="85aef-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="85aef-118">De lo contrario, \_ se devuelve lb bien (0).</span><span class="sxs-lookup"><span data-stu-id="85aef-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="85aef-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85aef-119">Remarks</span></span>

<span data-ttu-id="85aef-120">Si este mensaje se envía a un cuadro de lista de selección única que no contiene un elemento seleccionado, el índice del símbolo de intercalación se establece en el elemento especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="85aef-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="85aef-121">Si el cuadro de lista de selección única contiene un elemento seleccionado, el cuadro de lista devuelve LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="85aef-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="85aef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85aef-122">Requirements</span></span>



| <span data-ttu-id="85aef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="85aef-123">Requirement</span></span> | <span data-ttu-id="85aef-124">Value</span><span class="sxs-lookup"><span data-stu-id="85aef-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85aef-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85aef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85aef-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85aef-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85aef-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85aef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85aef-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="85aef-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85aef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85aef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="85aef-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85aef-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85aef-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="85aef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85aef-132">**LB \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="85aef-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





