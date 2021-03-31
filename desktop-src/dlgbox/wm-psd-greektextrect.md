---
title: Mensaje de WM_PSD_GREEKTEXTRECT (commdlg. h)
description: Notifica al procedimiento de enlace un cuadro de diálogo de configuración de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar texto griego dentro del rectángulo de margen de la página de ejemplo.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079575"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="e9058-104">\_ \_ Mensaje GREEKTEXTRECT de WM PSD</span><span class="sxs-lookup"><span data-stu-id="e9058-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="e9058-105">Notifica al procedimiento de enlace un cuadro de diálogo de **configuración de página** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar texto griego dentro del rectángulo de margen de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9058-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="e9058-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9058-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9058-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9058-108">Identificador del contexto de dispositivo para la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9058-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="e9058-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9058-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9058-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo de texto griego.</span><span class="sxs-lookup"><span data-stu-id="e9058-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9058-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9058-111">Return value</span></span>

<span data-ttu-id="e9058-112">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no dibuja la parte de texto griego de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9058-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="e9058-113">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo dibuja la parte de texto griego de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9058-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9058-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9058-114">Remarks</span></span>

<span data-ttu-id="e9058-115">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="e9058-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="e9058-116">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9058-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="e9058-117">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="e9058-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9058-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9058-118">Requirements</span></span>



| <span data-ttu-id="e9058-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9058-119">Requirement</span></span> | <span data-ttu-id="e9058-120">Value</span><span class="sxs-lookup"><span data-stu-id="e9058-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9058-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9058-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9058-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e9058-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9058-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9058-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9058-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9058-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9058-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9058-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9058-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9058-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9058-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9058-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9058-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e9058-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9058-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="e9058-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="e9058-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9058-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9058-131">**\_PAGESETUPDLG de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9058-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="e9058-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e9058-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9058-133">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="e9058-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

