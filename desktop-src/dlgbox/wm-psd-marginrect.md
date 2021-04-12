---
title: Mensaje de WM_PSD_MARGINRECT (commdlg. h)
description: Notifica al procedimiento de enlace un cuadro de diálogo de configuración de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar el rectángulo de margen de la página de ejemplo.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491860"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="3fd40-104">\_ \_ Mensaje MARGINRECT de WM PSD</span><span class="sxs-lookup"><span data-stu-id="3fd40-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="3fd40-105">Notifica al procedimiento de enlace un cuadro de diálogo de **configuración de página** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar el rectángulo de margen de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3fd40-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="3fd40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fd40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd40-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fd40-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd40-108">Identificador del contexto de dispositivo para la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3fd40-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="3fd40-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fd40-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd40-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, del rectángulo del margen.</span><span class="sxs-lookup"><span data-stu-id="3fd40-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd40-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fd40-111">Return value</span></span>

<span data-ttu-id="3fd40-112">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no dibuja el rectángulo de margen en la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3fd40-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="3fd40-113">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo dibuja el rectángulo de margen en la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3fd40-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd40-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd40-114">Remarks</span></span>

<span data-ttu-id="3fd40-115">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="3fd40-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="3fd40-116">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3fd40-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="3fd40-117">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="3fd40-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd40-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd40-118">Requirements</span></span>



| <span data-ttu-id="3fd40-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd40-119">Requirement</span></span> | <span data-ttu-id="3fd40-120">Value</span><span class="sxs-lookup"><span data-stu-id="3fd40-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd40-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fd40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd40-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3fd40-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3fd40-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fd40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd40-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3fd40-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3fd40-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fd40-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd40-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd40-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd40-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fd40-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fd40-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3fd40-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3fd40-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="3fd40-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="3fd40-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fd40-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3fd40-131">**\_PAGESETUPDLG de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="3fd40-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="3fd40-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3fd40-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3fd40-133">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="3fd40-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

