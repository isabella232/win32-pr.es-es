---
title: Mensaje de SB_SETTEXT (commctrl. h)
description: Establece el texto de la parte especificada de una ventana de estado.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150748"
---
# <a name="sb_settext-message"></a><span data-ttu-id="448ff-104">Mensaje de SETTEXT de SB \_</span><span class="sxs-lookup"><span data-stu-id="448ff-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="448ff-105">Establece el texto de la parte especificada de una ventana de estado.</span><span class="sxs-lookup"><span data-stu-id="448ff-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="448ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="448ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448ff-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="448ff-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="448ff-108">El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de la palabra de orden inferior especifica el índice de base cero del elemento que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="448ff-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="448ff-109">Si **LOBYTE** se establece en SB \_ SIMPLEID, se supone que la ventana de estado es una barra de estado de modo simple; es decir, una barra de estado con una sola parte.</span><span class="sxs-lookup"><span data-stu-id="448ff-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="448ff-110">El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de la palabra de orden inferior especifica el tipo de la operación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="448ff-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="448ff-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="448ff-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="448ff-112">Se omite la palabra de orden superior de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="448ff-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="448ff-113">Value</span><span class="sxs-lookup"><span data-stu-id="448ff-113">Value</span></span></th>
<th><span data-ttu-id="448ff-114">Significado</span><span class="sxs-lookup"><span data-stu-id="448ff-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="448ff-115"><dt><strong>0,1</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-116">El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="448ff-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="448ff-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-118">El texto se dibuja sin bordes.</span><span class="sxs-lookup"><span data-stu-id="448ff-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="448ff-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-120">El texto se dibuja mediante la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="448ff-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="448ff-121">Una barra de estado de modo simple no admite el dibujo del propietario.</span><span class="sxs-lookup"><span data-stu-id="448ff-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="448ff-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-123">El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.</span><span class="sxs-lookup"><span data-stu-id="448ff-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="448ff-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-125">El texto se mostrará en la dirección opuesta al texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="448ff-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="448ff-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="448ff-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="448ff-127">Se omiten los caracteres de tabulación.</span><span class="sxs-lookup"><span data-stu-id="448ff-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="448ff-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="448ff-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="448ff-129">Puntero a una cadena terminada en null que especifica el texto que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="448ff-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="448ff-130">Si *wParam* es SBT \_ OWNERDRAW, este parámetro representa 32 bits de datos.</span><span class="sxs-lookup"><span data-stu-id="448ff-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="448ff-131">La ventana primaria debe interpretar los datos y dibujar el texto cuando recibe el mensaje [**de \_ DRAWITEM de WM**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="448ff-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448ff-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="448ff-132">Return value</span></span>

<span data-ttu-id="448ff-133">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="448ff-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="448ff-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="448ff-134">Remarks</span></span>

<span data-ttu-id="448ff-135">El mensaje invalida la parte de la ventana que ha cambiado, lo que hace que muestre el nuevo texto cuando la ventana siguiente recibe el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="448ff-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="448ff-136">Texto normal de la pantalla de Windows de izquierda a derecha (LTR).</span><span class="sxs-lookup"><span data-stu-id="448ff-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="448ff-137">Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL).</span><span class="sxs-lookup"><span data-stu-id="448ff-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="448ff-138">Si \_ se establece SBT RTLREADING, la cadena *lParam* leerá en la dirección opuesta del texto de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="448ff-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="448ff-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="448ff-139">Requirements</span></span>



| <span data-ttu-id="448ff-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="448ff-140">Requirement</span></span> | <span data-ttu-id="448ff-141">Value</span><span class="sxs-lookup"><span data-stu-id="448ff-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="448ff-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="448ff-142">Minimum supported client</span></span><br/> | <span data-ttu-id="448ff-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="448ff-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="448ff-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="448ff-144">Minimum supported server</span></span><br/> | <span data-ttu-id="448ff-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="448ff-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="448ff-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="448ff-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="448ff-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="448ff-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="448ff-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="448ff-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="448ff-149">**SB \_ SETTEXTW** (Unicode) y **SB \_ SETTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="448ff-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="448ff-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="448ff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448ff-151">**GETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="448ff-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

