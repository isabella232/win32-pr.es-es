---
title: Mensaje de ICM_GETDEFAULTQUALITY (VFW. h)
description: El \_ mensaje GETDEFAULTQUALITY ICM consulta un controlador de compresión de vídeo para proporcionar la configuración de calidad predeterminada. Puede enviar este mensaje explícitamente o mediante la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- Mensaje de ICM_GETDEFAULTQUALITY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489592"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="826a7-105">\_Mensaje GETDEFAULTQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="826a7-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="826a7-106">El **mensaje \_ GETDEFAULTQUALITY ICM** consulta un controlador de compresión de vídeo para proporcionar la configuración de calidad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="826a7-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="826a7-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="826a7-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="826a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="826a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826a7-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="826a7-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="826a7-110">Dirección que va a contener el valor de calidad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="826a7-110">Address to contain the default quality value.</span></span> <span data-ttu-id="826a7-111">Los valores de calidad oscilan entre 0 y 10.000.</span><span class="sxs-lookup"><span data-stu-id="826a7-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826a7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="826a7-112">Return Value</span></span>

<span data-ttu-id="826a7-113">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="826a7-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="826a7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826a7-114">Requirements</span></span>



| <span data-ttu-id="826a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="826a7-115">Requirement</span></span> | <span data-ttu-id="826a7-116">Value</span><span class="sxs-lookup"><span data-stu-id="826a7-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="826a7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="826a7-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="826a7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="826a7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="826a7-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="826a7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="826a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="826a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="826a7-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="826a7-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826a7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="826a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826a7-124">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="826a7-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="826a7-125">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="826a7-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





