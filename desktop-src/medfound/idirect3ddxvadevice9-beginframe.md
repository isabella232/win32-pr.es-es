---
description: Comienza el procesamiento para crear una imagen descodificada.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9:: BeginFrame (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715888"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="175a2-103">IDirect3DDXVADevice9:: BeginFrame (método)</span><span class="sxs-lookup"><span data-stu-id="175a2-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="175a2-104">Comienza el procesamiento para crear una imagen descodificada.</span><span class="sxs-lookup"><span data-stu-id="175a2-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="175a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="175a2-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="175a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="175a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="175a2-107">*pDstSurface*</span><span class="sxs-lookup"><span data-stu-id="175a2-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="175a2-108">Puntero a la interfaz **IDirect3DSurface9** de la superficie de destino sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="175a2-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="175a2-109">*SizeInputData*</span><span class="sxs-lookup"><span data-stu-id="175a2-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="175a2-110">Tamaño del búfer especificado por *pInputData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="175a2-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="175a2-111">El valor debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="175a2-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="175a2-112">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="175a2-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="175a2-113">Puntero a un búfer que contiene datos para el acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="175a2-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="175a2-114">Este búfer debe contener el índice de marco basado en cero, especificado como un valor de **palabra** .</span><span class="sxs-lookup"><span data-stu-id="175a2-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="175a2-115">*pSizeOutputData*</span><span class="sxs-lookup"><span data-stu-id="175a2-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="175a2-116">Tamaño del búfer especificado por *pOutputData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="175a2-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="175a2-117">El valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="175a2-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="175a2-118">*pOutputData*</span><span class="sxs-lookup"><span data-stu-id="175a2-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="175a2-119">Puntero a un búfer en el que puede escribir el acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="175a2-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="175a2-120">Establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="175a2-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="175a2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="175a2-121">Return value</span></span>

<span data-ttu-id="175a2-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="175a2-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="175a2-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="175a2-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="175a2-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="175a2-124">Remarks</span></span>

<span data-ttu-id="175a2-125">Para cada llamada a **BeginFrame**, el descodificador debe hacer una llamada correspondiente a [**IDirect3DDXVADevice9:: EndFrame**](idirect3ddxvadevice9-endframe.md).</span><span class="sxs-lookup"><span data-stu-id="175a2-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="175a2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="175a2-126">Requirements</span></span>



| <span data-ttu-id="175a2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="175a2-127">Requirement</span></span> | <span data-ttu-id="175a2-128">Value</span><span class="sxs-lookup"><span data-stu-id="175a2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="175a2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="175a2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="175a2-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="175a2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="175a2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="175a2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="175a2-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="175a2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="175a2-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="175a2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="175a2-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="175a2-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175a2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="175a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175a2-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="175a2-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




