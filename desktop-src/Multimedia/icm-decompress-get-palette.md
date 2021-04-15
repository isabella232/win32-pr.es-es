---
title: Mensaje de ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: El \_ mensaje de la paleta descomprime ICM \_ Get \_ solicita que el controlador de descompresión de vídeo proporcione la tabla de colores de la estructura BITMAPINFOHEADER de salida. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- Mensaje de ICM_DECOMPRESS_GET_PALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676895"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="79674-105">Descomprime el \_ \_ mensaje de \_ paleta get de ICM</span><span class="sxs-lookup"><span data-stu-id="79674-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="79674-106">El mensaje de la **\_ \_ \_ paleta descomprime ICM Get** solicita que el controlador de descompresión de vídeo proporcione la tabla de colores de la estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de salida.</span><span class="sxs-lookup"><span data-stu-id="79674-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="79674-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="79674-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="79674-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79674-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79674-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="79674-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="79674-110">Puntero a una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="79674-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="79674-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="79674-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="79674-112">Puntero a una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contiene la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="79674-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="79674-113">El espacio reservado para la tabla de colores siempre tiene al menos 256 colores.</span><span class="sxs-lookup"><span data-stu-id="79674-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="79674-114">Puede especificar cero para que este parámetro devuelva solo el tamaño de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="79674-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79674-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79674-115">Return Value</span></span>

<span data-ttu-id="79674-116">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="79674-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79674-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79674-117">Remarks</span></span>

<span data-ttu-id="79674-118">Si *lpbiOutput* es distinto de cero, el controlador establece el miembro **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) en el número de colores de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="79674-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="79674-119">El controlador rellena el miembro **bmiColors** de [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con los colores reales.</span><span class="sxs-lookup"><span data-stu-id="79674-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="79674-120">El controlador solo debe admitir este mensaje si usa una paleta distinta de la especificada en el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="79674-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="79674-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79674-121">Requirements</span></span>



| <span data-ttu-id="79674-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79674-122">Requirement</span></span> | <span data-ttu-id="79674-123">Value</span><span class="sxs-lookup"><span data-stu-id="79674-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="79674-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79674-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79674-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="79674-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79674-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79674-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79674-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79674-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79674-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79674-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="79674-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="79674-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79674-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="79674-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79674-131">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="79674-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="79674-132">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="79674-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

