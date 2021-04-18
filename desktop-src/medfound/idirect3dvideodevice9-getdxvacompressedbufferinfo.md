---
description: Obtiene información acerca de los búferes comprimidos necesarios para la descodificación acelerada por hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715440"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="e8e79-103">IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo (método)</span><span class="sxs-lookup"><span data-stu-id="e8e79-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="e8e79-104">Obtiene información acerca de los búferes comprimidos necesarios para la descodificación acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="e8e79-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e79-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e8e79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8e79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e79-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="e8e79-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e79-108">Puntero a un GUID que especifica el perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="e8e79-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="e8e79-109">Para obtener una lista de los perfiles compatibles, llame a [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="e8e79-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e79-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="e8e79-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e79-111">Puntero a una estructura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica el tamaño y el formato de píxel de los datos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="e8e79-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="e8e79-112">*pNumBuffers*</span><span class="sxs-lookup"><span data-stu-id="e8e79-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e79-113">En la entrada, especifica el número de elementos de la matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="e8e79-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="e8e79-114">Si *pBufferInfo* es **null**, el valor de `*pNumBuffers` debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e8e79-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="e8e79-115">En la salida, si *pBufferInfo* es **null**, *pNumBuffers* recibe el tamaño de la matriz que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="e8e79-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="e8e79-116">De lo contrario, *pNumBuffers* recibe el número real de elementos que se copian en la matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="e8e79-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="e8e79-117">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="e8e79-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e79-118">Dirección de una matriz de estructuras [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="e8e79-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="e8e79-119">Si el valor no es **null**, el método copia una lista de estructuras **DXVACompBufferInfo** en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="e8e79-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="e8e79-120">Cada estructura corresponde a un tipo de búfer de datos comprimidos que usa el acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8e79-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="e8e79-121">Establezca todos los elementos de la matriz en cero antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="e8e79-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="e8e79-122">Cada índice de matriz corresponde a uno de los tipos de superficie de DXVA definidos en DXVA. h.</span><span class="sxs-lookup"><span data-stu-id="e8e79-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="e8e79-123">El acelerador de vídeo devuelve una lista de hasta **DXVA \_ tipos numéricos de \_ \_ \_ búfer** entradas de matriz.</span><span class="sxs-lookup"><span data-stu-id="e8e79-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="e8e79-124">Para obtener más información, consulte la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), sección 3,4, "lista de descripciones de búfer".</span><span class="sxs-lookup"><span data-stu-id="e8e79-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="e8e79-125">Si el perfil de DXVA no utiliza un tipo de búfer determinado, la entrada en dicho índice contiene ceros para todos los valores.</span><span class="sxs-lookup"><span data-stu-id="e8e79-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e79-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8e79-126">Return value</span></span>

<span data-ttu-id="e8e79-127">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e8e79-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8e79-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8e79-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e79-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e79-129">Requirements</span></span>



| <span data-ttu-id="e8e79-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e79-130">Requirement</span></span> | <span data-ttu-id="e8e79-131">Value</span><span class="sxs-lookup"><span data-stu-id="e8e79-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8e79-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e79-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e79-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e79-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8e79-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e79-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e79-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e79-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e8e79-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e79-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e79-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e79-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e79-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e79-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e79-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="e8e79-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
