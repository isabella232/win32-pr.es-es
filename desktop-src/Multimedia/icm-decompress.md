---
title: Mensaje de ICM_DECOMPRESS (VFW. h)
description: El \_ mensaje de descompresión ICM informa a un controlador de descompresión de vídeo para descomprimir un marco de datos en un búfer definido por la aplicación.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- Mensaje de ICM_DECOMPRESS de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079642"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="8d2eb-104">Descompresión de ICM \_</span><span class="sxs-lookup"><span data-stu-id="8d2eb-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="8d2eb-105">El mensaje de descompresión **ICM \_** informa a un controlador de descompresión de vídeo para descomprimir un marco de datos en un búfer definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="8d2eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d2eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d2eb-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="8d2eb-108">Puntero a una estructura [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d2eb-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8d2eb-110">Tamaño, en bytes, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span><span class="sxs-lookup"><span data-stu-id="8d2eb-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d2eb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d2eb-111">Return Value</span></span>

<span data-ttu-id="8d2eb-112">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d2eb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d2eb-113">Remarks</span></span>

<span data-ttu-id="8d2eb-114">Si desea que el controlador Descomprima los datos directamente en la pantalla, envíe el mensaje de [**\_ dibujo ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="8d2eb-115">El controlador devuelve un error si este mensaje se recibe antes del mensaje de [**\_ \_ Inicio de descompresión de ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="8d2eb-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d2eb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d2eb-116">Requirements</span></span>



| <span data-ttu-id="8d2eb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d2eb-117">Requirement</span></span> | <span data-ttu-id="8d2eb-118">Value</span><span class="sxs-lookup"><span data-stu-id="8d2eb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d2eb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d2eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d2eb-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d2eb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d2eb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d2eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d2eb-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d2eb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d2eb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d2eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d2eb-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d2eb-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d2eb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d2eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2eb-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="8d2eb-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8d2eb-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="8d2eb-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





