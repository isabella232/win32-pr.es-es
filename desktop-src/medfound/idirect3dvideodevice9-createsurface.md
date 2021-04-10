---
description: Crea una superficie comprimida para la descodificación de DirectX video Acceleration (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9:: CreateSurface (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156173"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="66488-103">IDirect3DVideoDevice9:: CreateSurface (método)</span><span class="sxs-lookup"><span data-stu-id="66488-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="66488-104">Crea una superficie comprimida para la descodificación de DirectX video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="66488-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="66488-105">Para obtener los requisitos de la superficie, llame a [**IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) y examine las estructuras [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) devueltas.</span><span class="sxs-lookup"><span data-stu-id="66488-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="66488-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66488-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="66488-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66488-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66488-108">*Width*</span><span class="sxs-lookup"><span data-stu-id="66488-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-109">Ancho de la superficie, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="66488-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="66488-110">Establezca este parámetro en **DXVACompBufferInfo. WidthToCreate**.</span><span class="sxs-lookup"><span data-stu-id="66488-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="66488-111">*Height*</span><span class="sxs-lookup"><span data-stu-id="66488-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-112">Alto de la superficie, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="66488-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="66488-113">Establezca este parámetro en **DXVACompBufferInfo. HeightToCreate**.</span><span class="sxs-lookup"><span data-stu-id="66488-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="66488-114">*Búferes de reserva*</span><span class="sxs-lookup"><span data-stu-id="66488-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-115">Número de búferes de reserva.</span><span class="sxs-lookup"><span data-stu-id="66488-115">The number of back buffers.</span></span> <span data-ttu-id="66488-116">Este parámetro puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="66488-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="66488-117">*Format*</span><span class="sxs-lookup"><span data-stu-id="66488-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-118">Formato de píxel, especificado como un valor de **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="66488-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="66488-119">Establezca este parámetro en **DXVACompBufferInfo. Format**.</span><span class="sxs-lookup"><span data-stu-id="66488-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="66488-120">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="66488-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-121">El bloque de memoria en el que se va a crear la superficie, especificado como un valor de **D3DPOOL** .</span><span class="sxs-lookup"><span data-stu-id="66488-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="66488-122">Establezca este parámetro en **DXVACompBufferInfo. Pool**.</span><span class="sxs-lookup"><span data-stu-id="66488-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="66488-123">*Uso*</span><span class="sxs-lookup"><span data-stu-id="66488-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-124">**Operación OR bit a bit** de una o varias constantes **D3DUSAGE** .</span><span class="sxs-lookup"><span data-stu-id="66488-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="66488-125">Establezca este parámetro en **DXVACompBufferInfo. Usage**.</span><span class="sxs-lookup"><span data-stu-id="66488-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="66488-126">*ppSurface*</span><span class="sxs-lookup"><span data-stu-id="66488-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-127">Recibe un puntero a la interfaz **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="66488-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="66488-128">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="66488-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="66488-129">*pSharedHandle*</span><span class="sxs-lookup"><span data-stu-id="66488-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="66488-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="66488-130">Reserved.</span></span> <span data-ttu-id="66488-131">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="66488-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66488-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66488-132">Return value</span></span>

<span data-ttu-id="66488-133">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="66488-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66488-134">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66488-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66488-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66488-135">Requirements</span></span>



| <span data-ttu-id="66488-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="66488-136">Requirement</span></span> | <span data-ttu-id="66488-137">Value</span><span class="sxs-lookup"><span data-stu-id="66488-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="66488-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66488-138">Minimum supported client</span></span><br/> | <span data-ttu-id="66488-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66488-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66488-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66488-140">Minimum supported server</span></span><br/> | <span data-ttu-id="66488-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66488-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66488-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66488-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="66488-143"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="66488-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66488-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="66488-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66488-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="66488-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




