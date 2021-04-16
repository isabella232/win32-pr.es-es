---
description: Usa la GPU para calcular la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica. Calcular la iluminación en la GPU generalmente será mucho más rápido que en la CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine:: ComputeDirectLightingSHGPU (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678853"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="3fd91-104">ID3DXPRTEngine:: ComputeDirectLightingSHGPU (método)</span><span class="sxs-lookup"><span data-stu-id="3fd91-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="3fd91-105">Usa la GPU para calcular la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica.</span><span class="sxs-lookup"><span data-stu-id="3fd91-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="3fd91-106">Calcular la iluminación en la GPU generalmente será mucho más rápido que en la CPU.</span><span class="sxs-lookup"><span data-stu-id="3fd91-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fd91-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="3fd91-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fd91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd91-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3fd91-111">Puntero al objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para ejecutar la simulación en la GPU.</span><span class="sxs-lookup"><span data-stu-id="3fd91-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="3fd91-112">El dispositivo debe admitir los sombreadores de píxeles de [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd91-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="3fd91-113">Las funciones de devolución de llamada no deben usar el objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que usa el simulador de GPU.</span><span class="sxs-lookup"><span data-stu-id="3fd91-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="3fd91-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fd91-116">Parámetro de simulación de GPU que define la resolución de la sombra del búfer de z.</span><span class="sxs-lookup"><span data-stu-id="3fd91-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="3fd91-117">Debe establecerse en uno de los valores constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span><span class="sxs-lookup"><span data-stu-id="3fd91-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="3fd91-118">Para especificar una simulación de precisión mayor, el \_ valor de D3DXSHGPUSIMOPT highquality puede combinarse con uno de los valores de D3DXSHGPUSIMOPT \_ SHADOWRESxxx.</span><span class="sxs-lookup"><span data-stu-id="3fd91-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="3fd91-119">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fd91-121">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="3fd91-121">Order of the SH evaluation.</span></span> <span data-ttu-id="3fd91-122">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="3fd91-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3fd91-123">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="3fd91-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3fd91-124">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="3fd91-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3fd91-125">*ZBias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fd91-127">Sesgo en la dirección normal.</span><span class="sxs-lookup"><span data-stu-id="3fd91-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="3fd91-128">*ZAngleBias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fd91-130">Sesgo en la dirección normal, escalada en una menos el coseno del ángulo con el rayo claro.</span><span class="sxs-lookup"><span data-stu-id="3fd91-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="3fd91-131">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3fd91-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd91-132">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3fd91-133">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd91-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="3fd91-134">Este búfer debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="3fd91-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd91-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fd91-135">Return value</span></span>

<span data-ttu-id="3fd91-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fd91-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fd91-137">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3fd91-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3fd91-138">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3fd91-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd91-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd91-139">Remarks</span></span>

<span data-ttu-id="3fd91-140">En este método, el albedo no se multiplica por la señal luminosa y solo se integra la luz entrante en el simulador.</span><span class="sxs-lookup"><span data-stu-id="3fd91-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="3fd91-141">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="3fd91-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="3fd91-142">Llame a [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia Radiance (PRT) precalculado por Albedo.</span><span class="sxs-lookup"><span data-stu-id="3fd91-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd91-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd91-143">Requirements</span></span>



| <span data-ttu-id="3fd91-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd91-144">Requirement</span></span> | <span data-ttu-id="3fd91-145">Value</span><span class="sxs-lookup"><span data-stu-id="3fd91-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd91-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fd91-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3fd91-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd91-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3fd91-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fd91-148">Library</span></span><br/> | <dl> <span data-ttu-id="3fd91-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fd91-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3fd91-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fd91-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd91-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3fd91-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
