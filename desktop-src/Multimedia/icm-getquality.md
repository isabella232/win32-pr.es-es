---
title: Mensaje de ICM_GETQUALITY (VFW. h)
description: El \_ mensaje GETQUALITY ICM consulta un controlador de compresión de vídeo para devolver su configuración de calidad actual.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- Mensaje de ICM_GETQUALITY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997161"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="98470-104">\_Mensaje GETQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="98470-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="98470-105">El **mensaje \_ GETQUALITY ICM** consulta un controlador de compresión de vídeo para devolver su configuración de calidad actual.</span><span class="sxs-lookup"><span data-stu-id="98470-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="98470-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98470-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98470-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="98470-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="98470-108">Dirección que va a contener el valor de calidad actual.</span><span class="sxs-lookup"><span data-stu-id="98470-108">Address to contain the current quality value.</span></span> <span data-ttu-id="98470-109">Los valores de calidad oscilan entre 0 y 10.000.</span><span class="sxs-lookup"><span data-stu-id="98470-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98470-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98470-110">Return Value</span></span>

<span data-ttu-id="98470-111">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98470-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98470-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98470-112">Requirements</span></span>



| <span data-ttu-id="98470-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98470-113">Requirement</span></span> | <span data-ttu-id="98470-114">Value</span><span class="sxs-lookup"><span data-stu-id="98470-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98470-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98470-115">Minimum supported client</span></span><br/> | <span data-ttu-id="98470-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98470-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98470-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98470-117">Minimum supported server</span></span><br/> | <span data-ttu-id="98470-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98470-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98470-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98470-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="98470-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="98470-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98470-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="98470-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98470-122">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="98470-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="98470-123">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="98470-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





