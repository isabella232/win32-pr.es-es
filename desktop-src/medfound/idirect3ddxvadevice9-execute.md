---
description: Realiza una operación de descodificación de DirectX video Acceleration (DXVA).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9:: Execute (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715887"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="b27c5-103">IDirect3DDXVADevice9:: Execute (método)</span><span class="sxs-lookup"><span data-stu-id="b27c5-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="b27c5-104">Realiza una operación de descodificación de DirectX video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="b27c5-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b27c5-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b27c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b27c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b27c5-107">*FunctionNum*</span><span class="sxs-lookup"><span data-stu-id="b27c5-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-108">**DWORD** que contiene uno o más números de función de DXVA.</span><span class="sxs-lookup"><span data-stu-id="b27c5-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="b27c5-109">Para obtener más información, consulte la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="b27c5-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-110">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="b27c5-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-111">Un puntero a un búfer que contiene los datos de entrada para la operación de descodificación.</span><span class="sxs-lookup"><span data-stu-id="b27c5-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="b27c5-112">El significado de estos datos depende del tipo de superficie y el número de función.</span><span class="sxs-lookup"><span data-stu-id="b27c5-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-113">*Inlocate*</span><span class="sxs-lookup"><span data-stu-id="b27c5-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-114">Tamaño de los datos de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b27c5-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="b27c5-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-116">Puntero a un búfer en el que el acelerador de vídeo escribe los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="b27c5-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-117">*Outlocate*</span><span class="sxs-lookup"><span data-stu-id="b27c5-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-118">Tamaño del búfer de *OutputData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="b27c5-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-119">*NumBuffers*</span><span class="sxs-lookup"><span data-stu-id="b27c5-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-120">Número de elementos de la matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="b27c5-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="b27c5-121">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="b27c5-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b27c5-122">Puntero a una matriz de estructuras [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="b27c5-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b27c5-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b27c5-123">Return value</span></span>

<span data-ttu-id="b27c5-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b27c5-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b27c5-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b27c5-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b27c5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b27c5-126">Requirements</span></span>



| <span data-ttu-id="b27c5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27c5-127">Requirement</span></span> | <span data-ttu-id="b27c5-128">Value</span><span class="sxs-lookup"><span data-stu-id="b27c5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b27c5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b27c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b27c5-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b27c5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b27c5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b27c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b27c5-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b27c5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b27c5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b27c5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27c5-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27c5-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27c5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b27c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27c5-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="b27c5-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
