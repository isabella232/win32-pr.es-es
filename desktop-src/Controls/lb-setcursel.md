---
title: Mensaje de LB_SETCURSEL (Winuser. h)
description: Selecciona una cadena y la desplaza a la vista, si es necesario. Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105648157"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="82ca2-105">\_Mensaje lb SETCURSEL</span><span class="sxs-lookup"><span data-stu-id="82ca2-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="82ca2-106">Selecciona una cadena y la desplaza a la vista, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="82ca2-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="82ca2-107">Cuando se selecciona la nueva cadena, el cuadro de lista quita el resaltado de la cadena seleccionada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="82ca2-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="82ca2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82ca2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ca2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82ca2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ca2-110">Especifica el índice de base cero de la cadena seleccionada.</span><span class="sxs-lookup"><span data-stu-id="82ca2-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="82ca2-111">Si este parámetro es-1, el cuadro de lista se establece para que no tenga ninguna selección.</span><span class="sxs-lookup"><span data-stu-id="82ca2-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="82ca2-112">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el parámetro *wParam* está limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="82ca2-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="82ca2-113">Esto significa que los cuadros de lista no pueden contener más de 32.767 elementos.</span><span class="sxs-lookup"><span data-stu-id="82ca2-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="82ca2-114">Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista está limitado únicamente por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="82ca2-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="82ca2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82ca2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="82ca2-116">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="82ca2-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ca2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82ca2-117">Return value</span></span>

<span data-ttu-id="82ca2-118">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="82ca2-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="82ca2-119">Si el parámetro *wParam* es-1, el valor devuelto es lb \_ Err aunque no se haya producido ningún error.</span><span class="sxs-lookup"><span data-stu-id="82ca2-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ca2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82ca2-120">Remarks</span></span>

<span data-ttu-id="82ca2-121">Use este mensaje solo con cuadros de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="82ca2-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="82ca2-122">No se puede utilizar para establecer o quitar una selección en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="82ca2-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ca2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ca2-123">Requirements</span></span>



| <span data-ttu-id="82ca2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ca2-124">Requirement</span></span> | <span data-ttu-id="82ca2-125">Value</span><span class="sxs-lookup"><span data-stu-id="82ca2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ca2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82ca2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="82ca2-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82ca2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="82ca2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82ca2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="82ca2-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="82ca2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="82ca2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82ca2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ca2-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82ca2-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ca2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="82ca2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ca2-133">**LB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="82ca2-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





