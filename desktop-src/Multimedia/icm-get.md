---
title: Mensaje de ICM_GET (VFW. h)
description: El \_ mensaje get de ICM recupera un valor DWORD definido por la aplicación de un controlador de compresión de vídeo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- Mensaje de ICM_GET de Windows multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801520"
---
# <a name="icm_get-message"></a><span data-ttu-id="5a6af-104">\_Obtener mensaje de ICM</span><span class="sxs-lookup"><span data-stu-id="5a6af-104">ICM\_GET message</span></span>

<span data-ttu-id="5a6af-105">El **mensaje \_ get de ICM** recupera un valor **DWORD** definido por la aplicación de un controlador de compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5a6af-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="5a6af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a6af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6af-107"><span id="pv"></span><span id="PV"></span>*FV*</span><span class="sxs-lookup"><span data-stu-id="5a6af-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="5a6af-108">Puntero a un bloque de memoria que se va a rellenar con el estado actual.</span><span class="sxs-lookup"><span data-stu-id="5a6af-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="5a6af-109">También puede especificar **null** para determinar la cantidad de memoria necesaria para la información de estado.</span><span class="sxs-lookup"><span data-stu-id="5a6af-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="5a6af-110"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="5a6af-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="5a6af-111">Tamaño, en bytes, del bloque de memoria.</span><span class="sxs-lookup"><span data-stu-id="5a6af-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6af-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a6af-112">Return Value</span></span>

<span data-ttu-id="5a6af-113">Devuelve la cantidad de memoria, en bytes, necesaria para almacenar la información de estado.</span><span class="sxs-lookup"><span data-stu-id="5a6af-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6af-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a6af-114">Remarks</span></span>

<span data-ttu-id="5a6af-115">La estructura utilizada para representar la información de estado es específica del controlador y está definida por el controlador.</span><span class="sxs-lookup"><span data-stu-id="5a6af-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6af-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a6af-116">Requirements</span></span>



| <span data-ttu-id="5a6af-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a6af-117">Requirement</span></span> | <span data-ttu-id="5a6af-118">Value</span><span class="sxs-lookup"><span data-stu-id="5a6af-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a6af-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a6af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6af-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a6af-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a6af-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a6af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6af-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a6af-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a6af-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a6af-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a6af-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a6af-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a6af-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a6af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6af-126">Administrador de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="5a6af-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5a6af-127">Mensajes de compresión de vídeo</span><span class="sxs-lookup"><span data-stu-id="5a6af-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





