---
title: Mensaje de MCIWNDM_REALIZE (VFW. h)
description: El mensaje de MCIWNDM de la \_ MCIWnd de la ventana de la ventana de una ventana de. Esta macro se define con el mensaje de MCIWNDM \_ . Puede enviar este mensaje explícitamente o mediante la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Mensaje de MCIWNDM_REALIZE de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995997"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="39ee1-106">Mensaje de MCIWNDM \_</span><span class="sxs-lookup"><span data-stu-id="39ee1-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="39ee1-107">El **mensaje \_ de MCIWNDM** de la MCIWnd de la ventana de la ventana de una ventana de.</span><span class="sxs-lookup"><span data-stu-id="39ee1-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="39ee1-108">Esta macro se define con el **mensaje \_ de MCIWNDM** .</span><span class="sxs-lookup"><span data-stu-id="39ee1-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="39ee1-109">Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="39ee1-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="39ee1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39ee1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ee1-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span><span class="sxs-lookup"><span data-stu-id="39ee1-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="39ee1-112">Marca de fondo.</span><span class="sxs-lookup"><span data-stu-id="39ee1-112">Background flag.</span></span> <span data-ttu-id="39ee1-113">Especifique **true** para este parámetro si la ventana es una aplicación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="39ee1-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ee1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39ee1-114">Return Value</span></span>

<span data-ttu-id="39ee1-115">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="39ee1-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39ee1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39ee1-116">Remarks</span></span>

<span data-ttu-id="39ee1-117">**MCIWNDM \_ En el uso se** usa la paleta del dispositivo MCI y se llama a la función [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) .</span><span class="sxs-lookup"><span data-stu-id="39ee1-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="39ee1-118">Si la aplicación controla explícitamente los mensajes de [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , debe usar este mensaje en la aplicación en lugar de usar **RealizePalette**.</span><span class="sxs-lookup"><span data-stu-id="39ee1-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="39ee1-119">Si el cuerpo de uno de estos controladores de mensajes contiene solo **RealizePalette**, reenvíe el mensaje a la ventana de MCIWnd, que obtendrá automáticamente la paleta.</span><span class="sxs-lookup"><span data-stu-id="39ee1-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ee1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ee1-120">Requirements</span></span>



| <span data-ttu-id="39ee1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ee1-121">Requirement</span></span> | <span data-ttu-id="39ee1-122">Value</span><span class="sxs-lookup"><span data-stu-id="39ee1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39ee1-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ee1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39ee1-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39ee1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39ee1-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ee1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39ee1-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39ee1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39ee1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39ee1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ee1-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ee1-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ee1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="39ee1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ee1-130">**MCIWndRealize**</span><span class="sxs-lookup"><span data-stu-id="39ee1-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="39ee1-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="39ee1-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="39ee1-132">**PALETTECHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="39ee1-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="39ee1-133">**QUERYNEWPALETTE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="39ee1-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

