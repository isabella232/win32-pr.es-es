---
title: Mensaje de ICM_COMPRESS_GET_FORMAT (VFW. h)
description: El \_ mensaje comprimir de ICM \_ obtener \_ formato solicita el formato de salida de los datos comprimidos de un controlador de compresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- Mensaje de ICM_COMPRESS_GET_FORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492359"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="eeeca-105">\_Mensaje de \_ obtención de formato de compresión \_ ICM</span><span class="sxs-lookup"><span data-stu-id="eeeca-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="eeeca-106">El **mensaje \_ comprimir de ICM \_ obtener \_ formato** solicita el formato de salida de los datos comprimidos de un controlador de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eeeca-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="eeeca-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="eeeca-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="eeeca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeeca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeeca-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="eeeca-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="eeeca-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="eeeca-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="eeeca-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="eeeca-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="eeeca-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="eeeca-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="eeeca-113">Puede especificar cero para que este parámetro solicite solo el tamaño del formato de salida, como en la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="eeeca-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeeca-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeeca-114">Return Value</span></span>

<span data-ttu-id="eeeca-115">Si *lpbiOutput* es cero, devuelve el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="eeeca-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="eeeca-116">Si *lpbiOutput* es distinto de cero, devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eeeca-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeeca-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeeca-117">Remarks</span></span>

<span data-ttu-id="eeeca-118">Si *lpbiOutput* es distinto de cero, el controlador debe rellenar la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con el formato de salida predeterminado correspondiente al formato de entrada especificado para *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="eeeca-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="eeeca-119">Si el compresor puede generar varios formatos, el formato predeterminado debe ser el que conserva la mayor cantidad de información.</span><span class="sxs-lookup"><span data-stu-id="eeeca-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeeca-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeeca-120">Requirements</span></span>



| <span data-ttu-id="eeeca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeeca-121">Requirement</span></span> | <span data-ttu-id="eeeca-122">Value</span><span class="sxs-lookup"><span data-stu-id="eeeca-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eeeca-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeeca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eeeca-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eeeca-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eeeca-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeeca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eeeca-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eeeca-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eeeca-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeeca-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeeca-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeeca-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeeca-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeeca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeeca-130">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eeeca-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="eeeca-131">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="eeeca-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

