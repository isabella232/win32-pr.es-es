---
title: Mensaje de ICM_DECOMPRESS_BEGIN (VFW. h)
description: El \_ mensaje de \_ Inicio de descompresión ICM informa a un controlador de descompresión de vídeo para preparar la descomprimición de los datos. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Mensaje de ICM_DECOMPRESS_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150871"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="d4644-105">\_Mensaje de inicio de descompresión ICM \_</span><span class="sxs-lookup"><span data-stu-id="d4644-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="d4644-106">El mensaje de **\_ \_ Inicio** de descompresión ICM informa a un controlador de descompresión de vídeo para preparar la descomprimición de los datos.</span><span class="sxs-lookup"><span data-stu-id="d4644-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="d4644-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="d4644-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="d4644-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4644-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="d4644-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="d4644-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="d4644-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="d4644-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="d4644-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="d4644-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="d4644-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4644-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4644-113">Return Value</span></span>

<span data-ttu-id="d4644-114">Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d4644-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4644-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4644-115">Remarks</span></span>

<span data-ttu-id="d4644-116">Cuando el controlador recibe este mensaje, debe asignar búferes y realizar operaciones que consumen mucho tiempo para que pueda procesar los mensajes de [**\_ descomprimir ICM**](icm-decompress.md) de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="d4644-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="d4644-117">Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="d4644-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="d4644-118">Los mensajes de **\_ \_ Inicio de descompresión de ICM** y [**\_ \_ fin de descompresión ICM**](icm-decompress-end.md) no se anidan.</span><span class="sxs-lookup"><span data-stu-id="d4644-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="d4644-119">Si el controlador recibe **el \_ \_ Inicio** de la descompresión ICM antes de que se detenga la descompresión con el **\_ \_ fin de descomprimir ICM**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="d4644-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4644-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4644-120">Requirements</span></span>



| <span data-ttu-id="d4644-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4644-121">Requirement</span></span> | <span data-ttu-id="d4644-122">Value</span><span class="sxs-lookup"><span data-stu-id="d4644-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4644-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4644-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d4644-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4644-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d4644-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4644-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d4644-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4644-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4644-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4644-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4644-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4644-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4644-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4644-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4644-130">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="d4644-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d4644-131">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="d4644-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

