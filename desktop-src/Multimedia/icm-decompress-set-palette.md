---
title: Mensaje de ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: El \_ mensaje de decompredor de la \_ paleta Set ICM \_ especifica una paleta para que un controlador de descompresión de vídeo lo use si se está descomprime con un formato que usa una paleta. Puede enviar este mensaje explícitamente o mediante la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Mensaje de ICM_DECOMPRESS_SET_PALETTE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676893"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="8832a-105">Descompresor ICM \_ \_ set \_ Palette Message</span><span class="sxs-lookup"><span data-stu-id="8832a-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="8832a-106">El mensaje de **\_ decompredor de la \_ \_ paleta Set ICM** especifica una paleta para que un controlador de descompresión de vídeo lo use si se está descomprime con un formato que usa una paleta.</span><span class="sxs-lookup"><span data-stu-id="8832a-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="8832a-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .</span><span class="sxs-lookup"><span data-stu-id="8832a-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="8832a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8832a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8832a-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span><span class="sxs-lookup"><span data-stu-id="8832a-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="8832a-110">Puntero a una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) cuya tabla de colores contiene los colores que se deben usar si es posible.</span><span class="sxs-lookup"><span data-stu-id="8832a-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="8832a-111">Puede especificar cero para usar el conjunto predeterminado de colores de salida.</span><span class="sxs-lookup"><span data-stu-id="8832a-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8832a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8832a-112">Return Value</span></span>

<span data-ttu-id="8832a-113">Devuelve ICERR \_ OK si el controlador de descompresión puede descomprimir imágenes con precisión en la paleta sugerida mediante el conjunto de colores que se organizan en la paleta.</span><span class="sxs-lookup"><span data-stu-id="8832a-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="8832a-114">Devuelve ICERR \_ no compatible en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8832a-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8832a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8832a-115">Remarks</span></span>

<span data-ttu-id="8832a-116">Este mensaje no debe afectar a la descompresión que ya está en curso; en su lugar, se deben devolver los colores que se pasan con este mensaje en respuesta a los mensajes de la paleta [**de obtención y \_ \_ \_**](icm-decompress-get-format.md) [**\_ descompresión \_ \_ ICM**](icm-decompress-get-palette.md) más adelante.</span><span class="sxs-lookup"><span data-stu-id="8832a-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="8832a-117">Los colores se devuelven al controlador de descompresión en un futuro mensaje de [**\_ \_ Inicio descomprimido de ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="8832a-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="8832a-118">Este mensaje se utiliza principalmente cuando un controlador descomprime imágenes en la pantalla y otra aplicación que usa una paleta está en primer plano, lo que obliga al controlador de descompresión a adaptarse a un conjunto de colores externo.</span><span class="sxs-lookup"><span data-stu-id="8832a-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="8832a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8832a-119">Requirements</span></span>



| <span data-ttu-id="8832a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8832a-120">Requirement</span></span> | <span data-ttu-id="8832a-121">Value</span><span class="sxs-lookup"><span data-stu-id="8832a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8832a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8832a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8832a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8832a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8832a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8832a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8832a-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8832a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8832a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8832a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8832a-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8832a-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8832a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8832a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8832a-129">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="8832a-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8832a-130">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="8832a-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

