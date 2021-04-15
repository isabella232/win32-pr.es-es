---
title: Mensaje LBSELCHSTRING (commdlg. h)
description: Un cuadro de diálogo abrir o guardar como envía el mensaje registrado LBSELCHSTRING al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Cuadros de diálogo de mensaje de LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14538c429bf943e4557974166bd7da747176bd93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695977"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="f19e7-104">Mensaje LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="f19e7-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="f19e7-105">\[A partir de Windows Vista, los cuadros de diálogo **abrir** y **Guardar como** común se han sustituido por el [cuadro de diálogo de elementos comunes](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f19e7-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="f19e7-106">Se recomienda usar la API de cuadros de diálogo de elementos comunes en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo comunes.\]</span><span class="sxs-lookup"><span data-stu-id="f19e7-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f19e7-107">Un cuadro de diálogo **abrir** o **Guardar como** envía el mensaje registrado **LBSELCHSTRING** al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f19e7-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="f19e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f19e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f19e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f19e7-110">Identificador del cuadro de lista o cuadro combinado en el que ha cambiado la selección.</span><span class="sxs-lookup"><span data-stu-id="f19e7-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="f19e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f19e7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f19e7-112">La palabra de orden inferior especifica el número de elemento de la cadena seleccionada en el cuadro de lista o el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="f19e7-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="f19e7-113">La palabra de orden superior especifica el tipo de cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="f19e7-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="f19e7-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f19e7-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f19e7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f19e7-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="f19e7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f19e7-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="f19e7-117"><dt>**CD \_ de LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f19e7-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="f19e7-118">El elemento es el único elemento seleccionado en un cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="f19e7-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="f19e7-119"><dt>**CD \_ de LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f19e7-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="f19e7-120">El elemento es uno de los elementos seleccionados en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="f19e7-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="f19e7-121"><dt>**CD \_ de LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f19e7-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="f19e7-122">El elemento ya no está seleccionado en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="f19e7-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="f19e7-123"><dt>**CD \_ de LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="f19e7-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="f19e7-124">No existe ningún elemento en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="f19e7-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19e7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f19e7-125">Return value</span></span>

<span data-ttu-id="f19e7-126">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f19e7-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19e7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f19e7-127">Remarks</span></span>

<span data-ttu-id="f19e7-128">El procedimiento de enlace debe especificar la constante **LBSELCHSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f19e7-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19e7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f19e7-129">Requirements</span></span>



| <span data-ttu-id="f19e7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19e7-130">Requirement</span></span> | <span data-ttu-id="f19e7-131">Value</span><span class="sxs-lookup"><span data-stu-id="f19e7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19e7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f19e7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f19e7-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f19e7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f19e7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f19e7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f19e7-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f19e7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f19e7-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f19e7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f19e7-137"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f19e7-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f19e7-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f19e7-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f19e7-139">**LBSELCHSTRINGW** (Unicode) y **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f19e7-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="f19e7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f19e7-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="f19e7-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f19e7-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f19e7-142">**SELCHANGE de CDN \_**</span><span class="sxs-lookup"><span data-stu-id="f19e7-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="f19e7-143">**TYPECHANGE de CDN \_**</span><span class="sxs-lookup"><span data-stu-id="f19e7-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="f19e7-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="f19e7-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="f19e7-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f19e7-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f19e7-146">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="f19e7-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

