---
title: Mensaje LBSELCHSTRING (Commdlg.h)
description: Un cuadro de diálogo Abrir o Guardar como envía el mensaje registrado LBSELCHSTRING al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Cuadros de diálogo del mensaje LBSELCHSTRING
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
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550050"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="04e3b-104">Mensaje LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="04e3b-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="04e3b-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="04e3b-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="04e3b-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="04e3b-107">Un **cuadro de** diálogo Abrir o Guardar como envía el mensaje registrado  **LBSELCHSTRING** al procedimiento de enlace cuando la selección cambia en cualquiera de los cuadros de lista o cuadros combinados del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="04e3b-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="04e3b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04e3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04e3b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04e3b-110">Identificador del cuadro de lista o cuadro combinado en el que cambió la selección.</span><span class="sxs-lookup"><span data-stu-id="04e3b-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="04e3b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04e3b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04e3b-112">La palabra de orden bajo especifica el número de elemento de la cadena seleccionada en el cuadro de lista o cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="04e3b-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="04e3b-113">La palabra de orden superior especifica el tipo de cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="04e3b-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="04e3b-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="04e3b-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="04e3b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="04e3b-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="04e3b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="04e3b-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="04e3b-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="04e3b-118">El elemento es el único elemento seleccionado en un cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="04e3b-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="04e3b-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="04e3b-120">El elemento es uno de los elementos seleccionados en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="04e3b-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="04e3b-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="04e3b-122">El elemento ya no está seleccionado en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="04e3b-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="04e3b-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="04e3b-124">No existe ningún elemento en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="04e3b-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e3b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04e3b-125">Return value</span></span>

<span data-ttu-id="04e3b-126">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="04e3b-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e3b-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04e3b-127">Remarks</span></span>

<span data-ttu-id="04e3b-128">El procedimiento de enlace debe especificar la **constante LBSELCHSTRING** en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener el identificador del mensaje enviado por el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="04e3b-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e3b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e3b-129">Requirements</span></span>



| <span data-ttu-id="04e3b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e3b-130">Requirement</span></span> | <span data-ttu-id="04e3b-131">Value</span><span class="sxs-lookup"><span data-stu-id="04e3b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e3b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04e3b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="04e3b-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04e3b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04e3b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04e3b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="04e3b-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04e3b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04e3b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04e3b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="04e3b-137"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="04e3b-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="04e3b-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="04e3b-139">**LBSELCHSTRINGW** (Unicode) y **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="04e3b-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="04e3b-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04e3b-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="04e3b-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="04e3b-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04e3b-142">**CDN \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="04e3b-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="04e3b-143">**CAMBIO DE \_ TIPO DE RED CDN**</span><span class="sxs-lookup"><span data-stu-id="04e3b-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="04e3b-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="04e3b-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="04e3b-145">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="04e3b-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04e3b-146">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="04e3b-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

