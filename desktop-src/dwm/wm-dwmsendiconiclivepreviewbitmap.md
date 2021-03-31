---
title: Mensaje de WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indica a una ventana que proporcione un mapa de bits estático para usarlo como vista previa dinámica (también conocida como vista previa de PEEK) de esa ventana.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490894"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="a4eee-104">Mensaje de DWMSENDICONICLIVEPREVIEWBITMAP de WM \_</span><span class="sxs-lookup"><span data-stu-id="a4eee-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="a4eee-105">Indica a una ventana que proporcione un mapa de bits estático para usarlo como *vista previa dinámica* (también conocida como *vista previa de PEEK*) de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="a4eee-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4eee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4eee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4eee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4eee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4eee-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a4eee-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a4eee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4eee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4eee-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a4eee-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4eee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4eee-111">Return value</span></span>

<span data-ttu-id="a4eee-112">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="a4eee-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4eee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4eee-113">Remarks</span></span>

<span data-ttu-id="a4eee-114">Una *vista previa dinámica* (también conocida como *vista previa PEEK*) de una ventana aparece cuando un usuario mueve el puntero del mouse sobre la miniatura de la ventana en la barra de tareas o le da el foco de miniatura en la ventana Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="a4eee-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="a4eee-115">Esta vista es una vista previa de tamaño completo de la ventana y puede ser una instantánea en directo o una representación de iconos.</span><span class="sxs-lookup"><span data-stu-id="a4eee-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="a4eee-116">Administrador de ventanas de escritorio (DWM) envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a4eee-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="a4eee-117">La vista previa dinámica se ha invocado en la ventana de.</span><span class="sxs-lookup"><span data-stu-id="a4eee-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="a4eee-118">El atributo DWMWA tiene el atributo de [**mapa de \_ \_ \_ bits de iconos**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) en la ventana.</span><span class="sxs-lookup"><span data-stu-id="a4eee-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="a4eee-119">Una representación de iconos es la única que existe para esta ventana.</span><span class="sxs-lookup"><span data-stu-id="a4eee-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="a4eee-120">La ventana que recibe este mensaje debe responder generando un mapa de bits a gran escala.</span><span class="sxs-lookup"><span data-stu-id="a4eee-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="a4eee-121">A continuación, la ventana llama a la función [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) para establecer la vista previa dinámica.</span><span class="sxs-lookup"><span data-stu-id="a4eee-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="a4eee-122">Si la ventana no establece un mapa de bits en un período de tiempo determinado, DWM usa su propia representación predeterminada de iconos para la ventana.</span><span class="sxs-lookup"><span data-stu-id="a4eee-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="a4eee-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a4eee-123">Examples</span></span>

<span data-ttu-id="a4eee-124">En el ejemplo siguiente se muestra una respuesta al mensaje de **\_ DWMSENDICONICLIVEPREVIEWBITMAP de WM** .</span><span class="sxs-lookup"><span data-stu-id="a4eee-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="a4eee-125">En el ejemplo se llama a la función [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un identificador para un mapa de bits personalizado independiente del dispositivo que se va a usar como representación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a4eee-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="a4eee-126">Para obtener el código completo, vea el ejemplo de cómo [personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="a4eee-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4eee-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4eee-127">Requirements</span></span>



| <span data-ttu-id="a4eee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4eee-128">Requirement</span></span> | <span data-ttu-id="a4eee-129">Value</span><span class="sxs-lookup"><span data-stu-id="a4eee-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4eee-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4eee-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a4eee-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4eee-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a4eee-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4eee-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a4eee-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4eee-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a4eee-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4eee-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4eee-135"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4eee-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4eee-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4eee-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4eee-137">**DWMSENDICONICTHUMBNAIL de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a4eee-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="a4eee-138">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="a4eee-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





