---
title: Mensaje de WM_PSD_PAGESETUPDLG (commdlg. h)
description: Notifica a un procedimiento de enlace PagePaintHook que el cuadro de diálogo Configurar página está a punto de dibujar el contenido de la página de ejemplo. El procedimiento de enlace puede utilizar este mensaje para llevar a cabo tareas de inicialización relacionadas con el dibujo del contenido de la página de ejemplo.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- WM_PSD_PAGESETUPDLG cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422589"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="59d20-105">\_ \_ Mensaje PAGESETUPDLG de WM PSD</span><span class="sxs-lookup"><span data-stu-id="59d20-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="59d20-106">Notifica a un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que el cuadro de diálogo **Configurar página** está a punto de dibujar el contenido de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="59d20-107">El procedimiento de enlace puede utilizar este mensaje para llevar a cabo tareas de inicialización relacionadas con el dibujo del contenido de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="59d20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59d20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d20-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59d20-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59d20-110">La palabra de orden inferior especifica un valor que indica el tamaño del papel.</span><span class="sxs-lookup"><span data-stu-id="59d20-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="59d20-111">Este valor puede ser uno de los valores de **DMPAPER \_** enumerados en la descripción de la estructura.</span><span class="sxs-lookup"><span data-stu-id="59d20-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="59d20-112">La palabra de orden superior especifica la orientación del papel o sobre, y si la impresora es un dispositivo de matriz de puntos o HPPCL (lenguaje de control de impresora de Hewlett Packard).</span><span class="sxs-lookup"><span data-stu-id="59d20-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="59d20-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="59d20-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="59d20-114">Valor</span><span class="sxs-lookup"><span data-stu-id="59d20-114">Value</span></span>                                                                             | <span data-ttu-id="59d20-115">Significado</span><span class="sxs-lookup"><span data-stu-id="59d20-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="59d20-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="59d20-117">Papel en modo horizontal (matriz de puntos)</span><span class="sxs-lookup"><span data-stu-id="59d20-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="59d20-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="59d20-119">Papel en modo horizontal (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="59d20-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="59d20-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="59d20-121">Papel en modo vertical (matriz de puntos)</span><span class="sxs-lookup"><span data-stu-id="59d20-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="59d20-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="59d20-123">Papel en modo vertical (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="59d20-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="59d20-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="59d20-125">Sobre en modo horizontal (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="59d20-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="59d20-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="59d20-127">Sobre en modo vertical (matriz de puntos)</span><span class="sxs-lookup"><span data-stu-id="59d20-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="59d20-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="59d20-129">Sobre en modo horizontal (matriz de puntos)</span><span class="sxs-lookup"><span data-stu-id="59d20-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="59d20-130"><dt>0x001f</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="59d20-131">Sobre en modo vertical (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="59d20-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="59d20-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59d20-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59d20-133">Puntero a una estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) que contiene la información utilizada para inicializar el cuadro de diálogo **Configurar página** .</span><span class="sxs-lookup"><span data-stu-id="59d20-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d20-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59d20-134">Return value</span></span>

<span data-ttu-id="59d20-135">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no envía más mensajes y no se dibuja en la página de ejemplo hasta la próxima vez que el sistema necesita volver a dibujar la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="59d20-136">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo envía el resto de los mensajes de la secuencia de dibujo.</span><span class="sxs-lookup"><span data-stu-id="59d20-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d20-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59d20-137">Remarks</span></span>

<span data-ttu-id="59d20-138">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="59d20-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="59d20-139">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="59d20-140">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="59d20-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="59d20-141">Los tres primeros mensajes de una secuencia de dibujo (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) proporcionan información que el procedimiento de enlace puede utilizar para dibujar el contenido de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="59d20-142">Los mensajes restantes ([**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notifican al procedimiento de enlace que el cuadro de diálogo está a punto de dibujar una parte específica de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="59d20-143">Esto permite al procedimiento de enlace dibujar de forma selectiva partes de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="59d20-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d20-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59d20-144">Requirements</span></span>



| <span data-ttu-id="59d20-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d20-145">Requirement</span></span> | <span data-ttu-id="59d20-146">Value</span><span class="sxs-lookup"><span data-stu-id="59d20-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d20-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59d20-147">Minimum supported client</span></span><br/> | <span data-ttu-id="59d20-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59d20-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="59d20-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59d20-149">Minimum supported server</span></span><br/> | <span data-ttu-id="59d20-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59d20-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59d20-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59d20-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d20-152"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59d20-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d20-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="59d20-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="59d20-154">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="59d20-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59d20-155">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="59d20-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="59d20-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59d20-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="59d20-157">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="59d20-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="59d20-158">**\_ENVSTAMPRECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="59d20-159">**\_FULLPAGERECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="59d20-160">**\_GREEKTEXTRECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="59d20-161">**\_MARGINRECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="59d20-162">**\_MINMARGINRECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="59d20-163">**\_YAFULLPAGERECT de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="59d20-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="59d20-164">**Vista**</span><span class="sxs-lookup"><span data-stu-id="59d20-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59d20-165">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="59d20-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

