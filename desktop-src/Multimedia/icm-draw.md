---
title: Mensaje de ICM_DRAW (VFW. h)
description: El \_ mensaje de dibujo ICM notifica a un controlador de representación que descomprima un fotograma de datos y lo dibuje en la pantalla.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- Mensaje de ICM_DRAW de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802029"
---
# <a name="icm_draw-message"></a><span data-ttu-id="65051-104">Mensaje de dibujo de ICM \_</span><span class="sxs-lookup"><span data-stu-id="65051-104">ICM\_DRAW message</span></span>

<span data-ttu-id="65051-105">El mensaje de **\_ dibujo ICM** notifica a un controlador de representación que descomprima un fotograma de datos y lo dibuje en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="65051-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="65051-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65051-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="65051-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="65051-108">Puntero a una estructura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .</span><span class="sxs-lookup"><span data-stu-id="65051-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="65051-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="65051-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="65051-110">Tamaño, en bytes, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span><span class="sxs-lookup"><span data-stu-id="65051-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65051-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65051-111">Return Value</span></span>

<span data-ttu-id="65051-112">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="65051-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65051-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65051-113">Remarks</span></span>

<span data-ttu-id="65051-114">Si la \_ marca de actualización ICDRAW se establece en el miembro **DwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), el área de la pantalla que se usa para dibujar no es válida y debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="65051-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="65051-115">La extensión de la actualización depende del contenido del miembro **lpData** .</span><span class="sxs-lookup"><span data-stu-id="65051-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="65051-116">Si **lpData** es **null**, el controlador debe actualizar el rectángulo de destino completo con la imagen actual.</span><span class="sxs-lookup"><span data-stu-id="65051-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="65051-117">Si el controlador mantiene una copia de la imagen en un búfer fuera de pantalla, puede producir un error en este mensaje.</span><span class="sxs-lookup"><span data-stu-id="65051-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="65051-118">Si **lpData** no es **null**, el controlador debe dibujar los datos y asegurarse de que se actualiza todo el destino.</span><span class="sxs-lookup"><span data-stu-id="65051-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="65051-119">Si la \_ marca ICDRAW HURRYUP se establece en **dwFlags**, la aplicación que realiza la llamada quiere que el controlador continúe lo más rápido posible, incluso aunque no actualice la pantalla.</span><span class="sxs-lookup"><span data-stu-id="65051-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="65051-120">Si \_ se establece la marca de preinstalación de ICDRAW en **dwFlags**, este fotograma de vídeo es información preliminar y no se debe mostrar si es posible.</span><span class="sxs-lookup"><span data-stu-id="65051-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="65051-121">Por ejemplo, si Play es empezar desde el fotograma 10 y el fotograma 0 es el fotograma clave anterior, los fotogramas del 0 al 9 tendrán establecido el preICDRAW \_ .</span><span class="sxs-lookup"><span data-stu-id="65051-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="65051-122">Si desea que el controlador Descomprima los datos en un búfer, envíe el mensaje de [**\_ descompresión ICM**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="65051-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="65051-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65051-123">Requirements</span></span>



| <span data-ttu-id="65051-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="65051-124">Requirement</span></span> | <span data-ttu-id="65051-125">Value</span><span class="sxs-lookup"><span data-stu-id="65051-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="65051-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65051-126">Minimum supported client</span></span><br/> | <span data-ttu-id="65051-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="65051-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="65051-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65051-128">Minimum supported server</span></span><br/> | <span data-ttu-id="65051-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65051-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="65051-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65051-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="65051-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="65051-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65051-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="65051-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65051-133">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="65051-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="65051-134">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="65051-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





