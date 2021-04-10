---
title: Mensaje de ICM_GETSTATE (VFW. h)
description: El \_ mensaje GETSTATE ICM consulta un controlador de compresión de vídeo para devolver su configuración actual en un bloque de memoria o para determinar la cantidad de memoria necesaria para recuperar la información de configuración.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- Mensaje de ICM_GETSTATE de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151242"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="c7132-104">\_Mensaje GETSTATE ICM</span><span class="sxs-lookup"><span data-stu-id="c7132-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="c7132-105">El **mensaje \_ GETSTATE ICM** consulta un controlador de compresión de vídeo para devolver su configuración actual en un bloque de memoria o para determinar la cantidad de memoria necesaria para recuperar la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="c7132-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="c7132-106">Puede enviar este mensaje explícitamente o mediante la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="c7132-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="c7132-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7132-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7132-108"><span id="pv"></span><span id="PV"></span>*FV*</span><span class="sxs-lookup"><span data-stu-id="c7132-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="c7132-109">Puntero a un bloque de memoria que va a contener la información de configuración actual.</span><span class="sxs-lookup"><span data-stu-id="c7132-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="c7132-110">Puede especificar **null** para este parámetro para determinar la cantidad de memoria necesaria para la información de configuración, como en [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="c7132-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="c7132-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="c7132-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="c7132-112">Tamaño, en bytes, del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="c7132-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7132-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7132-113">Return Value</span></span>

<span data-ttu-id="c7132-114">Si *PV* es **null**, devuelve la cantidad de memoria, en bytes, necesaria para la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="c7132-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="c7132-115">Si *PV* no es **null**, devuelve ICERR \_ OK si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c7132-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7132-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7132-116">Remarks</span></span>

<span data-ttu-id="c7132-117">La estructura que se usa para representar la información de configuración es específica del controlador y está definida por el controlador.</span><span class="sxs-lookup"><span data-stu-id="c7132-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7132-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7132-118">Requirements</span></span>



| <span data-ttu-id="c7132-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7132-119">Requirement</span></span> | <span data-ttu-id="c7132-120">Value</span><span class="sxs-lookup"><span data-stu-id="c7132-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7132-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7132-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7132-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7132-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c7132-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7132-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7132-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7132-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c7132-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7132-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7132-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7132-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7132-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7132-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7132-128">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="c7132-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c7132-129">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="c7132-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





