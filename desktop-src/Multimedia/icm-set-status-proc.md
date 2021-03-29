---
title: Mensaje de ICM_SET_STATUS_PROC (VFW. h)
description: El \_ mensaje del \_ procedimiento set \_ de estado de ICM proporciona una función de devolución de llamada de estado con el estado de una operación larga.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- Mensaje de ICM_SET_STATUS_PROC de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493282"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="374c6-104">\_Mensaje de procedimiento para establecer estado de ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="374c6-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="374c6-105">El mensaje del **\_ \_ \_ procedimiento set de estado de ICM** proporciona una función de devolución de llamada de estado con el estado de una operación larga.</span><span class="sxs-lookup"><span data-stu-id="374c6-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="374c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="374c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="374c6-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span><span class="sxs-lookup"><span data-stu-id="374c6-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="374c6-108">Puntero a una estructura [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="374c6-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="374c6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="374c6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="374c6-110">Tamaño, en bytes, de **ICSETSTATUSPROC**.</span><span class="sxs-lookup"><span data-stu-id="374c6-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="374c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="374c6-111">Return Value</span></span>

<span data-ttu-id="374c6-112">Devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="374c6-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="374c6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="374c6-113">Remarks</span></span>

<span data-ttu-id="374c6-114">La compatibilidad de este mensaje es opcional, pero se recomienda encarecidamente si la compresión o descompresión tarda más de aproximadamente una décima de segundo.</span><span class="sxs-lookup"><span data-stu-id="374c6-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="374c6-115">Una aplicación puede enviar este mensaje periódicamente a una función de devolución de llamada de estado durante las operaciones largas.</span><span class="sxs-lookup"><span data-stu-id="374c6-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="374c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="374c6-116">Requirements</span></span>



| <span data-ttu-id="374c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="374c6-117">Requirement</span></span> | <span data-ttu-id="374c6-118">Value</span><span class="sxs-lookup"><span data-stu-id="374c6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="374c6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="374c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="374c6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="374c6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="374c6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="374c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="374c6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="374c6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="374c6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="374c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="374c6-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="374c6-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="374c6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="374c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374c6-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="374c6-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="374c6-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="374c6-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





