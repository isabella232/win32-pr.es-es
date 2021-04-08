---
title: Mensaje de ICM_COMPRESS_GET_SIZE (VFW. h)
description: El \_ mensaje comprimir \_ de \_ tamaño del dispositivo Get size solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el formato de salida especificado. Puede enviar este mensaje explícitamente o mediante la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- Mensaje de ICM_COMPRESS_GET_SIZE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996898"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="e3a25-105">\_Mensaje de \_ obtención de tamaño de compresión \_ ICM</span><span class="sxs-lookup"><span data-stu-id="e3a25-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="e3a25-106">El mensaje comprimir de tamaño del dispositivo **\_ \_ Get \_ size** solicita que el controlador de compresión de vídeo proporcione el tamaño máximo de un fotograma de datos cuando se comprime en el formato de salida especificado.</span><span class="sxs-lookup"><span data-stu-id="e3a25-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="e3a25-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .</span><span class="sxs-lookup"><span data-stu-id="e3a25-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="e3a25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a25-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="e3a25-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="e3a25-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="e3a25-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="e3a25-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="e3a25-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="e3a25-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="e3a25-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a25-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3a25-113">Return Value</span></span>

<span data-ttu-id="e3a25-114">Devuelve el número máximo de bytes que puede ocupar un solo fotograma comprimido.</span><span class="sxs-lookup"><span data-stu-id="e3a25-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a25-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3a25-115">Remarks</span></span>

<span data-ttu-id="e3a25-116">Normalmente, las aplicaciones envían este mensaje para determinar el tamaño de un búfer que se va a asignar al marco comprimido.</span><span class="sxs-lookup"><span data-stu-id="e3a25-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="e3a25-117">El controlador debe calcular el tamaño del fotograma más grande posible en función de los formatos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="e3a25-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a25-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a25-118">Requirements</span></span>



| <span data-ttu-id="e3a25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a25-119">Requirement</span></span> | <span data-ttu-id="e3a25-120">Value</span><span class="sxs-lookup"><span data-stu-id="e3a25-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3a25-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a25-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e3a25-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e3a25-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3a25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a25-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e3a25-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3a25-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3a25-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3a25-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a25-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a25-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3a25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a25-128">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e3a25-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e3a25-129">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e3a25-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

