---
title: Mensaje de ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: El \_ mensaje de inicio DECOMPRESSEX de ICM notifica a \_ un controlador de compresión de vídeo que debe prepararse para descomprimir los datos.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Mensaje de ICM_DECOMPRESSEX_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803367"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="e1393-104">Mensaje de inicio de \_ DECOMPRESSEX ICM \_</span><span class="sxs-lookup"><span data-stu-id="e1393-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="e1393-105">El mensaje de **\_ \_ Inicio DECOMPRESSEX de ICM** notifica a un controlador de compresión de vídeo que debe prepararse para descomprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="e1393-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="e1393-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1393-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="e1393-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="e1393-108">Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene los formatos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="e1393-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="e1393-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1393-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e1393-110">Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="e1393-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1393-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1393-111">Return Value</span></span>

<span data-ttu-id="e1393-112">Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e1393-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1393-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1393-113">Remarks</span></span>

<span data-ttu-id="e1393-114">Cuando el controlador recibe este mensaje, debe asignar búferes y realizar operaciones que consumen mucho tiempo para que pueda procesar los [**mensajes \_ DECOMPRESSEX ICM**](icm-decompressex.md) de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="e1393-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="e1393-115">Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="e1393-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="e1393-116">Los mensajes de [**\_ \_ finalización**](icm-decompressex-end.md) de **DECOMPRESSEX de ICM \_ \_** y de fin de DECOMPRESSEX no se anidan.</span><span class="sxs-lookup"><span data-stu-id="e1393-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="e1393-117">Si el controlador recibe **el \_ \_ Inicio de DECOMPRESSEX ICM** antes de que se detenga la descompresión con **ICM \_ DECOMPRESSEX \_ End**, debe reiniciar la descompresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="e1393-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1393-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1393-118">Requirements</span></span>



| <span data-ttu-id="e1393-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1393-119">Requirement</span></span> | <span data-ttu-id="e1393-120">Value</span><span class="sxs-lookup"><span data-stu-id="e1393-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1393-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1393-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1393-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1393-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1393-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1393-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1393-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1393-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1393-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1393-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1393-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1393-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1393-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1393-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1393-128">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1393-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e1393-129">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1393-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





