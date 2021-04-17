---
description: Esta función, que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe. En su lugar, use D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Función D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653281"
---
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="a52f7-104">D3DX10ReflectShader función)</span><span class="sxs-lookup"><span data-stu-id="a52f7-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="a52f7-105">Esta función, que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe.</span><span class="sxs-lookup"><span data-stu-id="a52f7-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="a52f7-106">En su lugar, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span><span class="sxs-lookup"><span data-stu-id="a52f7-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a52f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a52f7-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="a52f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a52f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52f7-109">*pShaderBytecode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a52f7-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f7-110">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="a52f7-110">Type: **const void\***</span></span>

<span data-ttu-id="a52f7-111">Puntero al sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="a52f7-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="a52f7-112">Para obtener este puntero, vea [obtener un puntero a un sombreador compilado](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="a52f7-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="a52f7-113">*BytecodeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a52f7-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f7-114">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a52f7-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a52f7-115">Longitud de pShaderBytecode.</span><span class="sxs-lookup"><span data-stu-id="a52f7-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="a52f7-116">*ppReflector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a52f7-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a52f7-117">Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="a52f7-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="a52f7-118">Dirección de una interfaz de reflexión del sombreador (vea la [**interfaz ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).</span><span class="sxs-lookup"><span data-stu-id="a52f7-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a52f7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a52f7-119">Return value</span></span>

<span data-ttu-id="a52f7-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a52f7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a52f7-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a52f7-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a52f7-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a52f7-122">Remarks</span></span>

<span data-ttu-id="a52f7-123">Este es un ejemplo de creación de un objeto de reflexión de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a52f7-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="a52f7-124">En el ejemplo se da por supuesto que empieza con un sombreador compilado (mostrado como</span><span class="sxs-lookup"><span data-stu-id="a52f7-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="a52f7-125">que puede ver en el [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="a52f7-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a><span data-ttu-id="a52f7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a52f7-126">Requirements</span></span>



| <span data-ttu-id="a52f7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52f7-127">Requirement</span></span> | <span data-ttu-id="a52f7-128">Value</span><span class="sxs-lookup"><span data-stu-id="a52f7-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a52f7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a52f7-129">Header</span></span><br/> | <dl> <span data-ttu-id="a52f7-130"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52f7-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a52f7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a52f7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52f7-132">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="a52f7-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
