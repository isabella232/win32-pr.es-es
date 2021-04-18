---
title: Mensaje de ICM_DRAW_GETTIME (VFW. h)
description: El \_ \_ mensaje de creación de un controlador de presentación ICM solicita un controlador de representación que controla el tiempo de dibujo de los marcos para devolver el valor actual de su reloj interno. Puede enviar este mensaje explícitamente o mediante la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Mensaje de ICM_DRAW_GETTIME de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676800"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="f4f38-105">\_Mensaje GETTIME de Draw ICM \_</span><span class="sxs-lookup"><span data-stu-id="f4f38-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="f4f38-106">El mensaje de **\_ creación \_** de un controlador de presentación ICM solicita un controlador de representación que controla el tiempo de dibujo de los marcos para devolver el valor actual de su reloj interno.</span><span class="sxs-lookup"><span data-stu-id="f4f38-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="f4f38-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .</span><span class="sxs-lookup"><span data-stu-id="f4f38-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="f4f38-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4f38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f38-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span><span class="sxs-lookup"><span data-stu-id="f4f38-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="f4f38-110">Dirección que va a contener la hora actual.</span><span class="sxs-lookup"><span data-stu-id="f4f38-110">Address to contain the current time.</span></span> <span data-ttu-id="f4f38-111">El valor devuelto debe especificarse en los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="f4f38-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f38-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4f38-112">Return Value</span></span>

<span data-ttu-id="f4f38-113">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f4f38-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f38-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4f38-114">Remarks</span></span>

<span data-ttu-id="f4f38-115">Normalmente, este mensaje es compatible con hardware que realiza su propia descompresión asincrónica, temporización y dibujo.</span><span class="sxs-lookup"><span data-stu-id="f4f38-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="f4f38-116">También se puede enviar el mensaje si el hardware se utiliza como maestro de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f4f38-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f38-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f38-117">Requirements</span></span>



| <span data-ttu-id="f4f38-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f38-118">Requirement</span></span> | <span data-ttu-id="f4f38-119">Value</span><span class="sxs-lookup"><span data-stu-id="f4f38-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4f38-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f38-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f4f38-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f4f38-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f38-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4f38-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4f38-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4f38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4f38-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f38-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f38-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4f38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f38-127">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f4f38-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f4f38-128">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="f4f38-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





