---
title: Mensaje de ICM_SETSTATE (VFW. h)
description: El \_ mensaje de ICM SETSTATE informa a un controlador de compresión de vídeo para establecer el estado del compresor. Puede enviar este mensaje explícitamente o mediante la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- Mensaje de ICM_SETSTATE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677021"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="96c31-105">Mensaje de ICM \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="96c31-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="96c31-106">El mensaje de **ICM \_ SETSTATE** informa a un controlador de compresión de vídeo para establecer el estado del compresor.</span><span class="sxs-lookup"><span data-stu-id="96c31-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="96c31-107">Puede enviar este mensaje explícitamente o mediante la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="96c31-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="96c31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96c31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c31-109"><span id="pv"></span><span id="PV"></span>*FV*</span><span class="sxs-lookup"><span data-stu-id="96c31-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="96c31-110">Puntero a un bloque de memoria que contiene datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="96c31-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="96c31-111">Puede especificar **null** para este parámetro a fin de restablecer el compresor a su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="96c31-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="96c31-112"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="96c31-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="96c31-113">Tamaño, en bytes, del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="96c31-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c31-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96c31-114">Return Value</span></span>

<span data-ttu-id="96c31-115">Devuelve el número de bytes utilizados por el compresor si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="96c31-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c31-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96c31-116">Remarks</span></span>

<span data-ttu-id="96c31-117">La información que usa este mensaje es privada y específica de un compresor determinado.</span><span class="sxs-lookup"><span data-stu-id="96c31-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="96c31-118">Las aplicaciones cliente deben usar este mensaje solo para restaurar la información obtenida previamente con el mensaje [**\_ GETSTATE ICM**](icm-getstate.md) y deben usar el mensaje de [**\_ configuración de ICM**](icm-configure.md) para ajustar la configuración de un controlador de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="96c31-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c31-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c31-119">Requirements</span></span>



| <span data-ttu-id="96c31-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c31-120">Requirement</span></span> | <span data-ttu-id="96c31-121">Value</span><span class="sxs-lookup"><span data-stu-id="96c31-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96c31-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96c31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="96c31-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="96c31-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96c31-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96c31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="96c31-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96c31-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96c31-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96c31-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c31-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c31-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c31-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="96c31-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c31-129">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="96c31-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="96c31-130">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="96c31-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





