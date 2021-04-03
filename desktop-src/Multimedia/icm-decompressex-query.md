---
title: Mensaje de ICM_DECOMPRESSEX_QUERY (VFW. h)
description: El mensaje de consulta de DECOMPRESSEX ICM consulta \_ \_ un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- Mensaje de ICM_DECOMPRESSEX_QUERY de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905492"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="98869-104">Mensaje de consulta de \_ DECOMPRESSEX ICM \_</span><span class="sxs-lookup"><span data-stu-id="98869-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="98869-105">El mensaje de **\_ \_ consulta de DECOMPRESSEX ICM** consulta un controlador de compresión de vídeo para determinar si admite un formato de entrada específico o si puede descomprimir un formato de entrada específico en un formato de salida específico.</span><span class="sxs-lookup"><span data-stu-id="98869-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="98869-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98869-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="98869-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="98869-108">Puntero a una estructura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="98869-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="98869-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="98869-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="98869-110">Tamaño, en bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="98869-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98869-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98869-111">Return Value</span></span>

<span data-ttu-id="98869-112">Devuelve ICERR \_ OK si se admite la descompresión especificada o ICERR \_ BADFORMAT en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98869-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98869-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98869-113">Requirements</span></span>



| <span data-ttu-id="98869-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98869-114">Requirement</span></span> | <span data-ttu-id="98869-115">Value</span><span class="sxs-lookup"><span data-stu-id="98869-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98869-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98869-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98869-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98869-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98869-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98869-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98869-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98869-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98869-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98869-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98869-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="98869-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98869-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="98869-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98869-123">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="98869-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="98869-124">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="98869-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





