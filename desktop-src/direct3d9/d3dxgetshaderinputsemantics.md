---
description: Obtiene la semántica de las entradas del sombreador. Use este método para determinar el formato del vértice de entrada.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Función D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717759"
---
# <a name="d3dxgetshaderinputsemantics-function"></a><span data-ttu-id="a79c1-104">D3DXGetShaderInputSemantics función)</span><span class="sxs-lookup"><span data-stu-id="a79c1-104">D3DXGetShaderInputSemantics function</span></span>

<span data-ttu-id="a79c1-105">Obtiene la semántica de las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a79c1-105">Gets the semantics for the shader inputs.</span></span> <span data-ttu-id="a79c1-106">Use este método para determinar el formato del vértice de entrada.</span><span class="sxs-lookup"><span data-stu-id="a79c1-106">Use this method to determine the input vertex format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79c1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a79c1-107">Syntax</span></span>


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="a79c1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a79c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a79c1-109">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a79c1-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a79c1-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a79c1-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a79c1-111">Puntero a la secuencia DWORD de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a79c1-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="a79c1-112">*pSemantics* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a79c1-112">*pSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a79c1-113">Tipo: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***</span><span class="sxs-lookup"><span data-stu-id="a79c1-113">Type: **[**D3DXSEMANTIC**](d3dxsemantic.md)\***</span></span>

<span data-ttu-id="a79c1-114">Puntero a una matriz de estructuras [**D3DXSEMANTIC**](d3dxsemantic.md) .</span><span class="sxs-lookup"><span data-stu-id="a79c1-114">Pointer to an array of [**D3DXSEMANTIC**](d3dxsemantic.md) structures.</span></span> <span data-ttu-id="a79c1-115">La función rellenará esta matriz con la semántica de cada elemento de entrada al que hace referencia el sombreador.</span><span class="sxs-lookup"><span data-stu-id="a79c1-115">The function will fill this array with the semantics for each input element referenced by the shader.</span></span> <span data-ttu-id="a79c1-116">Se supone que esta matriz contiene al menos elementos MAXD3DDECLLENGTH.</span><span class="sxs-lookup"><span data-stu-id="a79c1-116">This array is assumed to contain at least MAXD3DDECLLENGTH elements.</span></span> <span data-ttu-id="a79c1-117">Sin embargo, si se llama a **D3DXGetShaderInputSemantics** con PSemantics = **null** , se devolverá el número de elementos necesarios para pCount.</span><span class="sxs-lookup"><span data-stu-id="a79c1-117">However, calling **D3DXGetShaderInputSemantics** with pSemantics = **NULL** will return the number of elements needed for pCount.</span></span>

</dd> <dt>

<span data-ttu-id="a79c1-118">*pCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a79c1-118">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a79c1-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a79c1-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a79c1-120">Devuelve el número de elementos de pSemantics.</span><span class="sxs-lookup"><span data-stu-id="a79c1-120">Returns the number of elements in pSemantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a79c1-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a79c1-121">Return value</span></span>

<span data-ttu-id="a79c1-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a79c1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a79c1-123">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a79c1-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a79c1-124">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a79c1-124">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a79c1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a79c1-125">Remarks</span></span>

<span data-ttu-id="a79c1-126">Use **D3DXGetShaderInputSemantics** para devolver una lista de semántica de entrada requerida por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="a79c1-126">Use **D3DXGetShaderInputSemantics** to return a list of input semantics required by the shader.</span></span> <span data-ttu-id="a79c1-127">Esta es la manera de averiguar cuál es el formato de vértice de entrada para un sombreador de lenguaje de sombreado de alto nivel (HLSL).</span><span class="sxs-lookup"><span data-stu-id="a79c1-127">This is the way to find out what the input vertex format is for a high-level shader language (HLSL) shader.</span></span> <span data-ttu-id="a79c1-128">Si el sombreador tiene entradas adicionales que faltan en la declaración de vértices, puede crear una secuencia de vértices adicional que tenga un paso de 0 que tenga los componentes que faltan con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="a79c1-128">If the shader has additional inputs that your vertex declaration is missing, you could create an extra vertex stream that has a stride of 0 that has the missing components with default values.</span></span> <span data-ttu-id="a79c1-129">Por ejemplo, esta técnica se puede usar para proporcionar el color de vértice predeterminado para los modelos que no la especifican.</span><span class="sxs-lookup"><span data-stu-id="a79c1-129">For instance, this technique could be used to provide default vertex color for models that do not specify it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a79c1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a79c1-130">Requirements</span></span>



| <span data-ttu-id="a79c1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a79c1-131">Requirement</span></span> | <span data-ttu-id="a79c1-132">Value</span><span class="sxs-lookup"><span data-stu-id="a79c1-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a79c1-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a79c1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a79c1-134"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a79c1-134"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a79c1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a79c1-135">Library</span></span><br/> | <dl> <span data-ttu-id="a79c1-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a79c1-136"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a79c1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a79c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79c1-138">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="a79c1-138">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
