---
description: Obtiene los nombres de muestra a los que se hace referencia en un sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Función D3DXGetShaderSamplers (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717757"
---
# <a name="d3dxgetshadersamplers-function"></a><span data-ttu-id="d143c-103">D3DXGetShaderSamplers función)</span><span class="sxs-lookup"><span data-stu-id="d143c-103">D3DXGetShaderSamplers function</span></span>

<span data-ttu-id="d143c-104">Obtiene los nombres de muestra a los que se hace referencia en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="d143c-104">Get the sampler names referenced in a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d143c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d143c-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="d143c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d143c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d143c-107">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d143c-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d143c-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d143c-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d143c-109">Puntero a la secuencia DWORD de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d143c-109">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="d143c-110">*pSamplers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d143c-110">*pSamplers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d143c-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d143c-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d143c-112">Puntero a una matriz de LPCSTRs.</span><span class="sxs-lookup"><span data-stu-id="d143c-112">Pointer to an array of LPCSTRs.</span></span> <span data-ttu-id="d143c-113">La función rellenará esta matriz con punteros a los nombres de muestra contenidos dentro de *pFunction*.</span><span class="sxs-lookup"><span data-stu-id="d143c-113">The function will fill this array with pointers to the sampler names contained within *pFunction*.</span></span> <span data-ttu-id="d143c-114">El tamaño máximo de la matriz es el número máximo de registros de muestra (16 para vs \_ 3 \_ 0 y PS \_ 3 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="d143c-114">The maximum array size is the maximum number of sampler registers (16 for vs\_3\_0 and ps\_3\_0).</span></span>

<span data-ttu-id="d143c-115">Para buscar el número de muestras usadas, compruebe *pCount* después de llamar a **D3DXGetShaderSamplers** con pSamplers = **null**.</span><span class="sxs-lookup"><span data-stu-id="d143c-115">To find the number of samplers used, check *pCount* after calling **D3DXGetShaderSamplers** with pSamplers = **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d143c-116">*pCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d143c-116">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d143c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d143c-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d143c-118">Devuelve el número de muestras a las que hace referencia el sombreador.</span><span class="sxs-lookup"><span data-stu-id="d143c-118">Returns the number of samplers referenced by the shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d143c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d143c-119">Return value</span></span>

<span data-ttu-id="d143c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d143c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d143c-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d143c-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d143c-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d143c-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d143c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d143c-123">Requirements</span></span>



| <span data-ttu-id="d143c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d143c-124">Requirement</span></span> | <span data-ttu-id="d143c-125">Value</span><span class="sxs-lookup"><span data-stu-id="d143c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d143c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d143c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d143c-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d143c-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d143c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d143c-128">Library</span></span><br/> | <dl> <span data-ttu-id="d143c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d143c-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d143c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d143c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d143c-131">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="d143c-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
