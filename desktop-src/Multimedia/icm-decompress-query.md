---
title: Mensaje de ICM_DECOMPRESS_QUERY (VFW. h)
description: El \_ mensaje de consulta de descomprimir ICM consulta \_ un controlador de descompresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- Mensaje de ICM_DECOMPRESS_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676894"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="b5100-104">Descomprime el \_ \_ mensaje de consulta</span><span class="sxs-lookup"><span data-stu-id="b5100-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="b5100-105">El mensaje de **\_ \_ consulta de descomprimir ICM** consulta un controlador de descompresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.</span><span class="sxs-lookup"><span data-stu-id="b5100-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="b5100-106">Puede enviar este mensaje explícitamente o mediante la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .</span><span class="sxs-lookup"><span data-stu-id="b5100-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="b5100-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5100-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5100-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="b5100-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="b5100-109">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="b5100-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="b5100-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="b5100-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="b5100-111">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="b5100-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="b5100-112">Puede especificar cero para que este parámetro indique que el formato de salida es aceptable.</span><span class="sxs-lookup"><span data-stu-id="b5100-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5100-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5100-113">Return Value</span></span>

<span data-ttu-id="b5100-114">Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b5100-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5100-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5100-115">Requirements</span></span>



| <span data-ttu-id="b5100-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5100-116">Requirement</span></span> | <span data-ttu-id="b5100-117">Value</span><span class="sxs-lookup"><span data-stu-id="b5100-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5100-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5100-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5100-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5100-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b5100-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5100-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5100-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5100-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5100-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5100-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5100-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5100-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5100-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5100-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5100-125">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="b5100-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b5100-126">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="b5100-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

