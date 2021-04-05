---
title: Mensaje de WM_PSD_YAFULLPAGERECT (commdlg. h)
description: Notifica al procedimiento de enlace un cuadro de diálogo de configuración de página, PagePaintHook, que el cuadro de diálogo está a punto de dibujar la parte de la dirección de retorno de una página de ejemplo de sobre.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079725"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="b919e-104">\_ \_ Mensaje YAFULLPAGERECT de WM PSD</span><span class="sxs-lookup"><span data-stu-id="b919e-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="b919e-105">Notifica al procedimiento de enlace un cuadro de diálogo de **configuración de página** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que el cuadro de diálogo está a punto de dibujar la parte de la dirección de retorno de una página de ejemplo de sobre.</span><span class="sxs-lookup"><span data-stu-id="b919e-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="b919e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b919e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b919e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b919e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b919e-108">Identificador del contexto de dispositivo para la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b919e-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="b919e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b919e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b919e-110">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b919e-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b919e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b919e-111">Return value</span></span>

<span data-ttu-id="b919e-112">Si el procedimiento de enlace devuelve **true**, el cuadro de diálogo no dibuja la parte de la dirección de retorno de una página de ejemplo de sobre.</span><span class="sxs-lookup"><span data-stu-id="b919e-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="b919e-113">Si el procedimiento de enlace devuelve **false**, el cuadro de diálogo dibuja la parte de la dirección de retorno de una página de ejemplo de sobre.</span><span class="sxs-lookup"><span data-stu-id="b919e-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="b919e-114">Si el tipo de papel no es un sobre, el valor devuelto no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b919e-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="b919e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b919e-115">Remarks</span></span>

<span data-ttu-id="b919e-116">El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="b919e-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="b919e-117">Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b919e-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="b919e-118">Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="b919e-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b919e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b919e-119">Requirements</span></span>



| <span data-ttu-id="b919e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b919e-120">Requirement</span></span> | <span data-ttu-id="b919e-121">Value</span><span class="sxs-lookup"><span data-stu-id="b919e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b919e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b919e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b919e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b919e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b919e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b919e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b919e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b919e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b919e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b919e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b919e-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b919e-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b919e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b919e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b919e-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b919e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b919e-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="b919e-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="b919e-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b919e-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b919e-132">**\_PAGESETUPDLG de PSD de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b919e-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="b919e-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b919e-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b919e-134">Biblioteca de cuadros de diálogo comunes</span><span class="sxs-lookup"><span data-stu-id="b919e-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

