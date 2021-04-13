---
title: Mensaje de WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492658"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="07924-104">Mensaje de DWMSENDICONICTHUMBNAIL de WM \_</span><span class="sxs-lookup"><span data-stu-id="07924-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="07924-105">Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.</span><span class="sxs-lookup"><span data-stu-id="07924-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="07924-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07924-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07924-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07924-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07924-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="07924-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="07924-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07924-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07924-110">El [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de este valor es la coordenada x máxima de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="07924-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="07924-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la coordenada y máxima.</span><span class="sxs-lookup"><span data-stu-id="07924-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="07924-112">Si una miniatura tiene una dimensión que supera uno o ambos valores, el DWM no acepta la miniatura.</span><span class="sxs-lookup"><span data-stu-id="07924-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07924-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07924-113">Return value</span></span>

<span data-ttu-id="07924-114">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="07924-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07924-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07924-115">Remarks</span></span>

<span data-ttu-id="07924-116">DWM envía este mensaje a una ventana si se cumplen todas las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="07924-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="07924-117">DWM muestra una representación icónica de la ventana.</span><span class="sxs-lookup"><span data-stu-id="07924-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="07924-118">El atributo DWMWA tiene el atributo de [**mapa de \_ \_ \_ bits de iconos**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) en la ventana.</span><span class="sxs-lookup"><span data-stu-id="07924-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="07924-119">La ventana no estableció un mapa de bits almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="07924-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="07924-120">Hay espacio en la memoria caché para otro mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="07924-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="07924-121">La ventana que recibe este mensaje debe responder generando un mapa de bits que no sea mayor que el tamaño solicitado en los parámetros del mensaje.</span><span class="sxs-lookup"><span data-stu-id="07924-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="07924-122">A continuación, la ventana llama a la función [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) para reemplazar la miniatura predeterminada.</span><span class="sxs-lookup"><span data-stu-id="07924-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="07924-123">Si la ventana no proporciona un mapa de bits en un período de tiempo determinado, DWM usa su propia representación predeterminada de iconos para la ventana.</span><span class="sxs-lookup"><span data-stu-id="07924-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="07924-124">La ventana debe pertenecer al proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="07924-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="07924-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="07924-125">Examples</span></span>

<span data-ttu-id="07924-126">En el ejemplo de código siguiente se muestra cómo responder al mensaje de **\_ DWMSENDICONICTHUMBNAIL de WM** .</span><span class="sxs-lookup"><span data-stu-id="07924-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="07924-127">En el ejemplo se llama a [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), con un identificador para un mapa de bits personalizado independiente del dispositivo que se va a usar como representación de Windows.</span><span class="sxs-lookup"><span data-stu-id="07924-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="07924-128">Para obtener el ejemplo completo, vea el ejemplo de cómo [personalizar una miniatura de iconos y un mapa de bits de vista previa dinámica](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="07924-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="07924-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07924-129">Requirements</span></span>



| <span data-ttu-id="07924-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="07924-130">Requirement</span></span> | <span data-ttu-id="07924-131">Value</span><span class="sxs-lookup"><span data-stu-id="07924-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07924-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07924-132">Minimum supported client</span></span><br/> | <span data-ttu-id="07924-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="07924-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="07924-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07924-134">Minimum supported server</span></span><br/> | <span data-ttu-id="07924-135">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="07924-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="07924-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07924-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="07924-137"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="07924-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07924-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="07924-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07924-139">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="07924-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="07924-140">**DWMSENDICONICLIVEPREVIEWBITMAP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="07924-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

