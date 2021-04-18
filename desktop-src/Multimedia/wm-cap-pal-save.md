---
title: Mensaje de WM_CAP_PAL_SAVE (VFW. h)
description: El mensaje de guardado de PAL de Cap de WM \_ \_ \_ guarda la paleta actual en un archivo de paleta. Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales. Puede enviar este mensaje explícitamente o mediante la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- Mensaje de WM_CAP_PAL_SAVE de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666028"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="05320-106">\_Mensaje de \_ guardado de PAL de Cap de WM \_</span><span class="sxs-lookup"><span data-stu-id="05320-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="05320-107">El mensaje de guardado de PAL de Cap de WM guarda la paleta actual en un archivo de paleta. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05320-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="05320-108">Los archivos de paleta suelen utilizar la extensión de nombre de archivo. Señales.</span><span class="sxs-lookup"><span data-stu-id="05320-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="05320-109">Puede enviar este mensaje explícitamente o mediante la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .</span><span class="sxs-lookup"><span data-stu-id="05320-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="05320-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05320-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05320-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="05320-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="05320-112">Puntero a una cadena terminada en null que contiene el nombre de archivo de la paleta.</span><span class="sxs-lookup"><span data-stu-id="05320-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05320-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05320-113">Return Value</span></span>

<span data-ttu-id="05320-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="05320-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="05320-115">Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.</span><span class="sxs-lookup"><span data-stu-id="05320-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="05320-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05320-116">Requirements</span></span>



| <span data-ttu-id="05320-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05320-117">Requirement</span></span> | <span data-ttu-id="05320-118">Value</span><span class="sxs-lookup"><span data-stu-id="05320-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05320-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05320-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05320-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="05320-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05320-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05320-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05320-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05320-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05320-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05320-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05320-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="05320-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05320-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="05320-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05320-126">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="05320-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="05320-127">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="05320-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





