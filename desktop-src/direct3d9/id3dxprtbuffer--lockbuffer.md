---
description: Bloquea un intervalo de datos de ejemplo de vértice o textura y obtiene un puntero a la ubicación en la memoria de búfer.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer:: LockBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2da8cb5a6a2e036fb7b495a129a5ef29d9ff749
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698311"
---
# <a name="id3dxprtbufferlockbuffer-method"></a><span data-ttu-id="cfc6e-103">ID3DXPRTBuffer:: LockBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="cfc6e-103">ID3DXPRTBuffer::LockBuffer method</span></span>

<span data-ttu-id="cfc6e-104">Bloquea un intervalo de datos de ejemplo de vértice o textura y obtiene un puntero a la ubicación en la memoria de búfer.</span><span class="sxs-lookup"><span data-stu-id="cfc6e-104">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfc6e-105">Syntax</span></span>


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="cfc6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfc6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc6e-107">*Iniciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfc6e-107">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc6e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc6e-109">Índice de la muestra de datos de vértice o textura.</span><span class="sxs-lookup"><span data-stu-id="cfc6e-109">Index of the sample of vertex or texel data.</span></span>

</dd> <dt>

<span data-ttu-id="cfc6e-110">*NumSamples* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfc6e-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc6e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc6e-112">Número de vértices (o textura) muestreados.</span><span class="sxs-lookup"><span data-stu-id="cfc6e-112">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="cfc6e-113">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfc6e-113">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc6e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cfc6e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="cfc6e-115">Puntero a la ubicación en memoria donde comienza el ejemplo de inicio.</span><span class="sxs-lookup"><span data-stu-id="cfc6e-115">Pointer to the location in memory where the Start sample begins.</span></span> <span data-ttu-id="cfc6e-116">El diseño de memoria de los datos del búfer es:</span><span class="sxs-lookup"><span data-stu-id="cfc6e-116">The memory layout of the buffer data is:</span></span>


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc6e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfc6e-117">Return value</span></span>

<span data-ttu-id="cfc6e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cfc6e-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cfc6e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cfc6e-120">Si se produce un error en el método, se devolverá el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="cfc6e-120">If the method fails, the following value will be returned:</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc6e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfc6e-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc6e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfc6e-122">Requirements</span></span>



| <span data-ttu-id="cfc6e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc6e-123">Requirement</span></span> | <span data-ttu-id="cfc6e-124">Value</span><span class="sxs-lookup"><span data-stu-id="cfc6e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc6e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfc6e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cfc6e-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc6e-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cfc6e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfc6e-127">Library</span></span><br/> | <dl> <span data-ttu-id="cfc6e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfc6e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cfc6e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfc6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc6e-130">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="cfc6e-130">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="cfc6e-131">**ID3DXPRTBuffer::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-131">**ID3DXPRTBuffer::GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[<span data-ttu-id="cfc6e-132">**ID3DXPRTBuffer::GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-132">**ID3DXPRTBuffer::GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[<span data-ttu-id="cfc6e-133">**ID3DXPRTBuffer::GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="cfc6e-133">**ID3DXPRTBuffer::GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
