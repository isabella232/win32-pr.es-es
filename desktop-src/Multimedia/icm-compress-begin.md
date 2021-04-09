---
title: Mensaje de ICM_COMPRESS_BEGIN (VFW. h)
description: El mensaje de inicio de compress de ICM \_ notifica a \_ un controlador de compresión de vídeo que debe prepararse para comprimir los datos. Puede enviar este mensaje explícitamente o mediante la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- Mensaje de ICM_COMPRESS_BEGIN de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079752"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="f23e9-105">Mensaje de inicio de \_ compresión ICM \_</span><span class="sxs-lookup"><span data-stu-id="f23e9-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="f23e9-106">El mensaje de **\_ \_ Inicio de compress de ICM** notifica a un controlador de compresión de vídeo que debe prepararse para comprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="f23e9-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="f23e9-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="f23e9-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="f23e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f23e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23e9-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="f23e9-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="f23e9-110">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="f23e9-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="f23e9-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="f23e9-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="f23e9-112">Puntero a una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contiene el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="f23e9-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f23e9-113">Return Value</span></span>

<span data-ttu-id="f23e9-114">Devuelve ICERR \_ OK si el controlador admite la compresión especificada o \_ BADFORMAT ICERR si no se admite el formato de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="f23e9-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="f23e9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f23e9-115">Remarks</span></span>

<span data-ttu-id="f23e9-116">El controlador debe asignar e inicializar las tablas o la memoria que necesita para comprimir los formatos de datos cuando recibe el mensaje [**de \_ compresión ICM**](icm-compress.md) .</span><span class="sxs-lookup"><span data-stu-id="f23e9-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="f23e9-117">VCM guarda la configuración del mensaje de **Inicio de \_ compresión \_ ICM** más reciente.</span><span class="sxs-lookup"><span data-stu-id="f23e9-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="f23e9-118">Los mensajes end **\_ compress \_ Begin** y [**ICM \_ compress \_**](icm-compress-end.md) no se anidan.</span><span class="sxs-lookup"><span data-stu-id="f23e9-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="f23e9-119">Si el controlador recibe la compresión de **ICM \_ \_ comienza** antes de que se detenga la compresión con el **\_ \_ fin de comprimir ICM**, debe reiniciar la compresión con nuevos parámetros.</span><span class="sxs-lookup"><span data-stu-id="f23e9-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23e9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f23e9-120">Requirements</span></span>



| <span data-ttu-id="f23e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23e9-121">Requirement</span></span> | <span data-ttu-id="f23e9-122">Value</span><span class="sxs-lookup"><span data-stu-id="f23e9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f23e9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f23e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f23e9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f23e9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f23e9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f23e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f23e9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f23e9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f23e9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f23e9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f23e9-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23e9-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23e9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f23e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23e9-130">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f23e9-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f23e9-131">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f23e9-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

