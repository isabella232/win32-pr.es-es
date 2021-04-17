---
title: Mensaje de ICM_COMPRESS_QUERY (VFW. h)
description: El mensaje de consulta de compresión ICM consulta \_ \_ un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede comprimir un formato de entrada específico a un formato de salida específico.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- Mensaje de ICM_COMPRESS_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676900"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="61c0b-104">Mensaje de consulta de \_ compresión ICM \_</span><span class="sxs-lookup"><span data-stu-id="61c0b-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="61c0b-105">El mensaje de **\_ \_ consulta** de compresión ICM consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede comprimir un formato de entrada específico a un formato de salida específico.</span><span class="sxs-lookup"><span data-stu-id="61c0b-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="61c0b-106">Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .</span><span class="sxs-lookup"><span data-stu-id="61c0b-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="61c0b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c0b-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="61c0b-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="61c0b-109">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="61c0b-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="61c0b-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="61c0b-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="61c0b-111">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="61c0b-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="61c0b-112">Puede especificar cero para que este parámetro indique que el formato de salida es aceptable.</span><span class="sxs-lookup"><span data-stu-id="61c0b-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61c0b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c0b-113">Return Value</span></span>

<span data-ttu-id="61c0b-114">Devuelve ICERR \_ OK si se admite la compresión especificada o ICERR \_ BADFORMAT en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="61c0b-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="61c0b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61c0b-115">Remarks</span></span>

<span data-ttu-id="61c0b-116">Cuando un controlador recibe este mensaje, debe examinar la estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) asociada a *lpbiInput* para determinar si puede comprimir el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="61c0b-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c0b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c0b-117">Requirements</span></span>



| <span data-ttu-id="61c0b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c0b-118">Requirement</span></span> | <span data-ttu-id="61c0b-119">Value</span><span class="sxs-lookup"><span data-stu-id="61c0b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="61c0b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c0b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="61c0b-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="61c0b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="61c0b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c0b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="61c0b-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61c0b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61c0b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61c0b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="61c0b-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="61c0b-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61c0b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="61c0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61c0b-127">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="61c0b-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="61c0b-128">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="61c0b-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

