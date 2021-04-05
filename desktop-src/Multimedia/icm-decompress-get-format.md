---
title: Mensaje de ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: El \_ \_ \_ mensaje de obtención de formato ICM descomprime solicita el formato de salida de los datos descomprimidos de un controlador de descompresión de vídeo. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- Mensaje de ICM_DECOMPRESS_GET_FORMAT de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079644"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="2b635-105">Descompresión ICM \_ \_ Get \_ Format Message</span><span class="sxs-lookup"><span data-stu-id="2b635-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="2b635-106">El mensaje de **\_ obtención de \_ \_ formato ICM descomprime** solicita el formato de salida de los datos descomprimidos de un controlador de descompresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2b635-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="2b635-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="2b635-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="2b635-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b635-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="2b635-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="2b635-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b635-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="2b635-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="2b635-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="2b635-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="2b635-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="2b635-113">Puede especificar cero para solicitar solo el tamaño del formato de salida, como en la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="2b635-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b635-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b635-114">Return Value</span></span>

<span data-ttu-id="2b635-115">Si *lpbiOutput* es cero, devuelve el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="2b635-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="2b635-116">Si *lpbiOutput* es distinto de cero, devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2b635-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b635-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b635-117">Remarks</span></span>

<span data-ttu-id="2b635-118">Si *lpbiOutput* es distinto de cero, el controlador debe rellenar la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con el formato de salida predeterminado correspondiente al formato de entrada especificado para *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="2b635-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="2b635-119">Si el compresor puede generar varios formatos, el formato predeterminado debe ser el que conserva la mayor cantidad de información.</span><span class="sxs-lookup"><span data-stu-id="2b635-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b635-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b635-120">Requirements</span></span>



| <span data-ttu-id="2b635-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b635-121">Requirement</span></span> | <span data-ttu-id="2b635-122">Value</span><span class="sxs-lookup"><span data-stu-id="2b635-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2b635-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b635-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b635-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2b635-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2b635-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b635-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b635-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b635-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b635-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b635-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b635-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b635-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b635-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b635-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b635-130">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2b635-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2b635-131">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="2b635-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

