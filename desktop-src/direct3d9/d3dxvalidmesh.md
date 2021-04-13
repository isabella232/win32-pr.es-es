---
description: Valida una malla.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Función D3DXValidMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362521"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="2d113-103">D3DXValidMesh función)</span><span class="sxs-lookup"><span data-stu-id="2d113-103">D3DXValidMesh function</span></span>

<span data-ttu-id="2d113-104">Valida una malla.</span><span class="sxs-lookup"><span data-stu-id="2d113-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d113-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d113-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="2d113-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d113-107">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d113-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d113-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="2d113-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="2d113-109">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="2d113-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="2d113-110">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d113-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d113-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d113-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d113-112">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla que se van a probar.</span><span class="sxs-lookup"><span data-stu-id="2d113-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="2d113-113">*ppErrorsAndWarnings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d113-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d113-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d113-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2d113-115">Devuelve un búfer que contiene una cadena de errores y advertencias, que explican los problemas encontrados en la malla.</span><span class="sxs-lookup"><span data-stu-id="2d113-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d113-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d113-116">Return value</span></span>

<span data-ttu-id="2d113-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d113-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d113-118">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d113-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d113-119">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DXERR \_ INVALIDMESH, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2d113-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d113-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d113-120">Remarks</span></span>

<span data-ttu-id="2d113-121">Este método valida la malla comprobando si hay índices no válidos.</span><span class="sxs-lookup"><span data-stu-id="2d113-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="2d113-122">La información del error está disponible en la salida del depurador.</span><span class="sxs-lookup"><span data-stu-id="2d113-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d113-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d113-123">Requirements</span></span>



| <span data-ttu-id="2d113-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d113-124">Requirement</span></span> | <span data-ttu-id="2d113-125">Value</span><span class="sxs-lookup"><span data-stu-id="2d113-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d113-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d113-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2d113-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d113-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2d113-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d113-128">Library</span></span><br/> | <dl> <span data-ttu-id="2d113-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d113-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d113-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d113-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d113-131">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="2d113-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
