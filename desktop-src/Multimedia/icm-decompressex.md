---
title: Mensaje de ICM_DECOMPRESSEX (VFW. h)
description: El \_ mensaje DECOMPRESSEX de ICM notifica a un controlador de compresión de vídeo que debe descomprimir un fotograma de datos directamente en la pantalla, descomprimir en un DIB en paralelo o descomprimir imágenes que se describen con los rectángulos de origen y de destino.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Mensaje de ICM_DECOMPRESSEX de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079641"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="a0e90-104">\_Mensaje DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="a0e90-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="a0e90-105">El **mensaje \_ DECOMPRESSEX de ICM** notifica a un controlador de compresión de vídeo que debe descomprimir un fotograma de datos directamente en la pantalla, descomprimir en un DIB en paralelo o descomprimir imágenes que se describen con los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="a0e90-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="a0e90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e90-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="a0e90-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="a0e90-108">Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .</span><span class="sxs-lookup"><span data-stu-id="a0e90-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0e90-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0e90-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a0e90-110">Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="a0e90-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0e90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0e90-111">Return Value</span></span>

<span data-ttu-id="a0e90-112">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a0e90-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e90-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0e90-113">Remarks</span></span>

<span data-ttu-id="a0e90-114">Este mensaje es similar a la descompresión de ICM, con la diferencia de que usa la estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir la información de descompresión. [**\_**](icm-decompress.md)</span><span class="sxs-lookup"><span data-stu-id="a0e90-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="a0e90-115">Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e90-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="a0e90-116">El controlador devuelve un error si este mensaje se recibe antes del mensaje de [**\_ \_ Inicio DECOMPRESSEX de ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e90-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e90-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0e90-117">Requirements</span></span>



| <span data-ttu-id="a0e90-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e90-118">Requirement</span></span> | <span data-ttu-id="a0e90-119">Value</span><span class="sxs-lookup"><span data-stu-id="a0e90-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a0e90-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0e90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e90-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a0e90-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a0e90-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0e90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e90-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a0e90-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0e90-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0e90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0e90-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e90-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e90-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0e90-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e90-127">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="a0e90-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a0e90-128">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="a0e90-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





