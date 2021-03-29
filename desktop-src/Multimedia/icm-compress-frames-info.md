---
title: Mensaje de ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: El \_ mensaje de información de tramas compress de ICM \_ \_ notifica a un controlador de compresión que establezca los parámetros para la compresión pendiente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- Mensaje de ICM_COMPRESS_FRAMES_INFO de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492358"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="acb2c-104">\_Mensaje de \_ información de marcos de compresión ICM \_</span><span class="sxs-lookup"><span data-stu-id="acb2c-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="acb2c-105">El mensaje de **\_ \_ \_ información de tramas compress de ICM** notifica a un controlador de compresión que establezca los parámetros para la compresión pendiente.</span><span class="sxs-lookup"><span data-stu-id="acb2c-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="acb2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acb2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb2c-107"><span id="icf"></span><span id="ICF"></span>*probar*</span><span class="sxs-lookup"><span data-stu-id="acb2c-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="acb2c-108">Puntero a una estructura [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) .</span><span class="sxs-lookup"><span data-stu-id="acb2c-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="acb2c-109">Los miembros **GetData** y **PutData** de esta estructura no se usan con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="acb2c-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="acb2c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="acb2c-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="acb2c-111">Tamaño, en bytes, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span><span class="sxs-lookup"><span data-stu-id="acb2c-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb2c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acb2c-112">Return Value</span></span>

<span data-ttu-id="acb2c-113">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="acb2c-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb2c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acb2c-114">Remarks</span></span>

<span data-ttu-id="acb2c-115">Un compresor puede usar este mensaje para determinar la cantidad de espacio que se va a asignar a cada fotograma durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="acb2c-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb2c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acb2c-116">Requirements</span></span>



| <span data-ttu-id="acb2c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb2c-117">Requirement</span></span> | <span data-ttu-id="acb2c-118">Value</span><span class="sxs-lookup"><span data-stu-id="acb2c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="acb2c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acb2c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="acb2c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="acb2c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="acb2c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acb2c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="acb2c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="acb2c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="acb2c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acb2c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb2c-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb2c-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb2c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="acb2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb2c-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="acb2c-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="acb2c-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="acb2c-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





