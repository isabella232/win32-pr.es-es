---
title: Mensaje de ICM_SETQUALITY (VFW. h)
description: El \_ mensaje SETQUALITY ICM proporciona un controlador de compresión de vídeo con un nivel de calidad que se utiliza durante la compresión.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- Mensaje de ICM_SETQUALITY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422633"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="d3979-104">\_Mensaje SETQUALITY ICM</span><span class="sxs-lookup"><span data-stu-id="d3979-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="d3979-105">El **mensaje \_ SETQUALITY ICM** proporciona un controlador de compresión de vídeo con un nivel de calidad que se utiliza durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="d3979-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="d3979-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3979-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="d3979-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="d3979-108">Nuevo valor de calidad.</span><span class="sxs-lookup"><span data-stu-id="d3979-108">New quality value.</span></span> <span data-ttu-id="d3979-109">Los valores de calidad oscilan entre 0 y 10.000.</span><span class="sxs-lookup"><span data-stu-id="d3979-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3979-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3979-110">Return Value</span></span>

<span data-ttu-id="d3979-111">Devuelve ICERR \_ OK si el controlador admite este mensaje o ICERR \_ no se admite en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d3979-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3979-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3979-112">Requirements</span></span>



| <span data-ttu-id="d3979-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3979-113">Requirement</span></span> | <span data-ttu-id="d3979-114">Value</span><span class="sxs-lookup"><span data-stu-id="d3979-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d3979-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3979-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d3979-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3979-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d3979-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3979-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d3979-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3979-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3979-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3979-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3979-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3979-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3979-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3979-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3979-122">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="d3979-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d3979-123">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="d3979-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





