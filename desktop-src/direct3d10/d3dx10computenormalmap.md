---
description: 'Función D3DX10ComputeNormalMap: convierte un mapa de alto en un mapa normal. Los componentes (x,y,z) de cada normal se asignan a los canales (r,g,b) de la textura de salida.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Función D3DX10ComputeNormalMap (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105323"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="80f68-104">Función D3DX10ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="80f68-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="80f68-105">Convierte un mapa de alto en un mapa normal.</span><span class="sxs-lookup"><span data-stu-id="80f68-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="80f68-106">Los componentes (x,y,z) de cada normal se asignan a los canales (r,g,b) de la textura de salida.</span><span class="sxs-lookup"><span data-stu-id="80f68-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f68-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80f68-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="80f68-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80f68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80f68-109">*pSrcTexture* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80f68-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f68-110">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="80f68-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="80f68-111">Puntero a una interfaz ID3D10Texture2D, que representa la textura del mapa de alto de origen.</span><span class="sxs-lookup"><span data-stu-id="80f68-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="80f68-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="80f68-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f68-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80f68-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80f68-114">Una o varias marcas NORMALMAP de D3DX \_ que controlan la generación de mapas normales.</span><span class="sxs-lookup"><span data-stu-id="80f68-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="80f68-115">*Canal* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80f68-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f68-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80f68-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80f68-117">Una marca D3DX \_ CHANNEL que especifica el origen de la información de alto.</span><span class="sxs-lookup"><span data-stu-id="80f68-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="80f68-118">*Amplitude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80f68-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f68-119">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80f68-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80f68-120">Multiplicador de valor constante que aumenta (o disminuye) los valores del mapa normal.</span><span class="sxs-lookup"><span data-stu-id="80f68-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="80f68-121">Los valores más altos suelen hacer que los aumentos sean más visibles, y los valores más bajos suelen hacer que los aumentos sean menos visibles.</span><span class="sxs-lookup"><span data-stu-id="80f68-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="80f68-122">*pDestTexture* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80f68-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f68-123">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="80f68-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="80f68-124">Puntero a una interfaz ID3D10Texture2D, que representa la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="80f68-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80f68-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80f68-125">Return value</span></span>

<span data-ttu-id="80f68-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80f68-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80f68-127">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80f68-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80f68-128">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="80f68-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="80f68-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80f68-129">Remarks</span></span>

<span data-ttu-id="80f68-130">Este método calcula lo normal mediante la diferencia central con un tamaño de kernel de 3x3.</span><span class="sxs-lookup"><span data-stu-id="80f68-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="80f68-131">Los canales RGB del destino contienen componentes sesgados (x, y,z) de lo normal.</span><span class="sxs-lookup"><span data-stu-id="80f68-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="80f68-132">El denominador de diferenciación central se codifica de forma rígida en 2.0.</span><span class="sxs-lookup"><span data-stu-id="80f68-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f68-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80f68-133">Requirements</span></span>



| <span data-ttu-id="80f68-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="80f68-134">Requirement</span></span> | <span data-ttu-id="80f68-135">Value</span><span class="sxs-lookup"><span data-stu-id="80f68-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80f68-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80f68-136">Header</span></span><br/>  | <dl> <span data-ttu-id="80f68-137"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="80f68-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="80f68-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80f68-138">Library</span></span><br/> | <dl> <span data-ttu-id="80f68-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="80f68-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="80f68-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80f68-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f68-141">Funciones de textura en D3DX 10</span><span class="sxs-lookup"><span data-stu-id="80f68-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
