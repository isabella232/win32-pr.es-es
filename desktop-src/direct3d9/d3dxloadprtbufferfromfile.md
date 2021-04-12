---
description: Carga en la memoria un búfer de Radiance Transfer (PRT) previamente calculado que se guardó en el disco.
ms.assetid: b9296c9e-e8ff-4a18-8682-fcac4feb64e9
title: Función D3DXLoadPRTBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10caedc9b77ef97f4d070ce82392b5da1de54fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362444"
---
# <a name="d3dxloadprtbufferfromfile-function"></a><span data-ttu-id="448ce-103">D3DXLoadPRTBufferFromFile función)</span><span class="sxs-lookup"><span data-stu-id="448ce-103">D3DXLoadPRTBufferFromFile function</span></span>

<span data-ttu-id="448ce-104">Carga en la memoria un búfer de Radiance Transfer (PRT) previamente calculado que se guardó en el disco.</span><span class="sxs-lookup"><span data-stu-id="448ce-104">Loads into memory a precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="448ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="448ce-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTBufferFromFile(
  _In_    LPCSTR          pFileName,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="448ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="448ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448ce-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="448ce-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448ce-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="448ce-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="448ce-109">Nombre del archivo desde el que se van a cargar los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="448ce-109">Name of the file from which to load the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="448ce-110">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="448ce-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="448ce-111">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="448ce-111">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="448ce-112">Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="448ce-112">Address of a pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448ce-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="448ce-113">Return value</span></span>

<span data-ttu-id="448ce-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="448ce-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="448ce-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="448ce-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="448ce-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="448ce-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="448ce-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="448ce-117">Remarks</span></span>

<span data-ttu-id="448ce-118">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="448ce-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="448ce-119">Si se define Unicode, la llamada de función se resuelve como D3DXLoadPRTBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="448ce-119">If Unicode is defined, the function call resolves to D3DXLoadPRTBufferFromFileW.</span></span> <span data-ttu-id="448ce-120">De lo contrario, la llamada de función se resuelve como D3DXLoadPRTBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="448ce-120">Otherwise, the function call resolves to D3DXLoadPRTBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="448ce-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="448ce-121">Requirements</span></span>



| <span data-ttu-id="448ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="448ce-122">Requirement</span></span> | <span data-ttu-id="448ce-123">Value</span><span class="sxs-lookup"><span data-stu-id="448ce-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="448ce-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="448ce-124">Header</span></span><br/>  | <dl> <span data-ttu-id="448ce-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="448ce-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="448ce-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="448ce-126">Library</span></span><br/> | <dl> <span data-ttu-id="448ce-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="448ce-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="448ce-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="448ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448ce-129">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="448ce-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
