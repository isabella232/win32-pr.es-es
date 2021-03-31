---
title: Mensaje de WM_PSD_FULLPAGERECT (commdlg. h)
description: Notifica a un procedimiento de enlace PagePaintHook las coordenadas del rectángulo de la página de ejemplo en el cuadro de diálogo Configurar página. El cuadro de diálogo envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- WM_PSD_FULLPAGERECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996767"
---
# <a name="wm_psd_fullpagerect-message"></a><span data-ttu-id="a6f63-105">\_ \_ Mensaje FULLPAGERECT de WM PSD</span><span class="sxs-lookup"><span data-stu-id="a6f63-105">WM\_PSD\_FULLPAGERECT message</span></span>

<span data-ttu-id="a6f63-106">Notifica a un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) las coordenadas del rectángulo de la página de ejemplo en el cuadro de diálogo **Configurar página** .</span><span class="sxs-lookup"><span data-stu-id="a6f63-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the sample page rectangle in the **Page Setup** dialog box.</span></span> <span data-ttu-id="a6f63-107">El cuadro de diálogo envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-107">The dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="a6f63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6f63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f63-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6f63-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f63-110">Identificador del contexto de dispositivo para la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="a6f63-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6f63-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f63-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6f63-113">Return value</span></span>

<span data-ttu-id="a6f63-114">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no envía más mensajes y no se dibuja en la página de ejemplo hasta la próxima vez que el sistema necesita volver a dibujar la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="a6f63-115">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo envía el resto de los mensajes de la secuencia de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f63-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6f63-116">Remarks</span></span>

<span data-ttu-id="a6f63-117">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="a6f63-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="a6f63-118">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a6f63-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="a6f63-119">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="a6f63-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6f63-120">Requirements</span></span>



| <span data-ttu-id="a6f63-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6f63-121">Requirement</span></span> | <span data-ttu-id="a6f63-122">Value</span><span class="sxs-lookup"><span data-stu-id="a6f63-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f63-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6f63-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f63-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a6f63-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a6f63-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6f63-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f63-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6f63-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6f63-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6f63-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6f63-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6f63-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f63-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6f63-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6f63-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a6f63-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6f63-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="a6f63-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="a6f63-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a6f63-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a6f63-133">**\_PAGESETUPDLG de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a6f63-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="a6f63-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a6f63-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6f63-135">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="a6f63-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

