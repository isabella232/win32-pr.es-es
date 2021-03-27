---
title: Función D3DX11ComputeNormalMap (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Función D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280436"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="e6f3c-105">D3DX11ComputeNormalMap función)</span><span class="sxs-lookup"><span data-stu-id="e6f3c-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="e6f3c-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6f3c-107">En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="e6f3c-108">Convierte un mapa de alto en un mapa normal.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="e6f3c-109">Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f3c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6f3c-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e6f3c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6f3c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f3c-112">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="e6f3c-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="e6f3c-114">Puntero a una interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) que representa la textura de mapa de alto de origen.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="e6f3c-115">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-116">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="e6f3c-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="e6f3c-117">Puntero a una interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura de mapa de alto de origen.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="e6f3c-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e6f3c-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e6f3c-120">Una o varias \_ marcas de NORMALMAP de D3DX que controlan la generación de asignaciones normales.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="e6f3c-121">*Canal* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e6f3c-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e6f3c-123">Una \_ marca de canal de D3DX que especifica el origen de la información de alto.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="e6f3c-124">*Amplitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e6f3c-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e6f3c-126">Multiplicador de valor constante que aumenta (o reduce) los valores del mapa normal.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="e6f3c-127">Los valores más altos normalmente hacen que los golpes sean más visibles, los valores más bajos normalmente hacen que los golpes sean menos visibles.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="e6f3c-128">*pDestTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6f3c-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f3c-129">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="e6f3c-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="e6f3c-130">Puntero a una interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f3c-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6f3c-131">Return value</span></span>

<span data-ttu-id="e6f3c-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6f3c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6f3c-133">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e6f3c-134">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6f3c-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6f3c-135">Remarks</span></span>

<span data-ttu-id="e6f3c-136">Este método calcula el normal mediante el uso de la diferencia central con el tamaño del kernel 3x3.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="e6f3c-137">Los canales RGB del destino contienen componentes sesgados (x, y, z) de la normal.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="e6f3c-138">El denominador de diferencia central se codifica en 2,0.</span><span class="sxs-lookup"><span data-stu-id="e6f3c-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f3c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6f3c-139">Requirements</span></span>



| <span data-ttu-id="e6f3c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f3c-140">Requirement</span></span> | <span data-ttu-id="e6f3c-141">Value</span><span class="sxs-lookup"><span data-stu-id="e6f3c-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f3c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6f3c-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e6f3c-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6f3c-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e6f3c-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6f3c-144">Library</span></span><br/> | <dl> <span data-ttu-id="e6f3c-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6f3c-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e6f3c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6f3c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f3c-147">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="e6f3c-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

