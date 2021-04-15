---
title: Mensaje de WM_PSD_ENVSTAMPRECT (commdlg. h)
description: Notifica al procedimiento de enlace un cuadro de diálogo de configuración de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar el rectángulo de la marca de sobre de la página de ejemplo.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- WM_PSD_ENVSTAMPRECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491861"
---
# <a name="wm_psd_envstamprect-message"></a><span data-ttu-id="d159b-104">\_ \_ Mensaje ENVSTAMPRECT de WM PSD</span><span class="sxs-lookup"><span data-stu-id="d159b-104">WM\_PSD\_ENVSTAMPRECT message</span></span>

<span data-ttu-id="d159b-105">Notifica al procedimiento de enlace un cuadro de diálogo de **configuración de página** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar el rectángulo de la marca de sobre de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d159b-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the envelope-stamp rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a><span data-ttu-id="d159b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d159b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d159b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d159b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d159b-108">Identificador del contexto de dispositivo para la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d159b-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="d159b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d159b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d159b-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo de la marca de sobre.</span><span class="sxs-lookup"><span data-stu-id="d159b-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the envelope-stamp rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d159b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d159b-111">Return value</span></span>

<span data-ttu-id="d159b-112">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no dibuja la parte de la marca de sobre de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d159b-112">If the hook procedure returns **TRUE**, the dialog box does not draw the envelope-stamp portion of the sample page.</span></span>

<span data-ttu-id="d159b-113">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo dibuja la parte de la marca de envoltura de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d159b-113">If the hook procedure returns **FALSE**, the dialog box draws the envelope-stamp portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="d159b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d159b-114">Remarks</span></span>

<span data-ttu-id="d159b-115">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="d159b-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="d159b-116">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d159b-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="d159b-117">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="d159b-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="d159b-118">Un procedimiento de enlace recibe este mensaje solo si el tipo de papel seleccionado es un sobre.</span><span class="sxs-lookup"><span data-stu-id="d159b-118">A hook procedure receives this message only if the selected paper type is an envelope.</span></span>

## <a name="requirements"></a><span data-ttu-id="d159b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d159b-119">Requirements</span></span>



| <span data-ttu-id="d159b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d159b-120">Requirement</span></span> | <span data-ttu-id="d159b-121">Value</span><span class="sxs-lookup"><span data-stu-id="d159b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d159b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d159b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d159b-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d159b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d159b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d159b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d159b-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d159b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d159b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d159b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d159b-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d159b-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d159b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d159b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d159b-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d159b-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d159b-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="d159b-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="d159b-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d159b-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d159b-132">**\_PAGESETUPDLG de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d159b-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="d159b-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d159b-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d159b-134">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="d159b-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

