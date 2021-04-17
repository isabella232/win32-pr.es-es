---
title: Mensaje de ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: El \_ mensaje GETDEFAULTKEYFRAMERATE ICM consulta un controlador de compresión de vídeo para obtener el espaciado de fotogramas clave predeterminado (o preferido). Puede enviar este mensaje explícitamente o mediante la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- Mensaje de ICM_GETDEFAULTKEYFRAMERATE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422369"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="68ec1-105">\_Mensaje GETDEFAULTKEYFRAMERATE ICM</span><span class="sxs-lookup"><span data-stu-id="68ec1-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="68ec1-106">El **mensaje \_ GETDEFAULTKEYFRAMERATE ICM** consulta un controlador de compresión de vídeo para obtener el espaciado de fotogramas clave predeterminado (o preferido).</span><span class="sxs-lookup"><span data-stu-id="68ec1-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="68ec1-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .</span><span class="sxs-lookup"><span data-stu-id="68ec1-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="68ec1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68ec1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ec1-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="68ec1-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="68ec1-110">Dirección que va a contener el espaciado de fotogramas de clave preferido.</span><span class="sxs-lookup"><span data-stu-id="68ec1-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ec1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68ec1-111">Return Value</span></span>

<span data-ttu-id="68ec1-112">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="68ec1-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ec1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68ec1-113">Requirements</span></span>



| <span data-ttu-id="68ec1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68ec1-114">Requirement</span></span> | <span data-ttu-id="68ec1-115">Value</span><span class="sxs-lookup"><span data-stu-id="68ec1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="68ec1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68ec1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="68ec1-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68ec1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="68ec1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68ec1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="68ec1-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68ec1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68ec1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68ec1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ec1-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ec1-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ec1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="68ec1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ec1-123">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="68ec1-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="68ec1-124">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="68ec1-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





