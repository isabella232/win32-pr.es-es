---
description: Carga en la memoria un búfer comprimido de Radiance Transfer (PRT) que se guardó en el disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Función D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362762"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="66598-103">D3DXLoadPRTCompBufferFromFile función)</span><span class="sxs-lookup"><span data-stu-id="66598-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="66598-104">Carga en la memoria un búfer comprimido de Radiance Transfer (PRT) que se guardó en el disco.</span><span class="sxs-lookup"><span data-stu-id="66598-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="66598-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66598-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="66598-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66598-107">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66598-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66598-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66598-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66598-109">Nombre del archivo desde el que se van a cargar los datos de búfer comprimidos.</span><span class="sxs-lookup"><span data-stu-id="66598-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="66598-110">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="66598-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66598-111">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="66598-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="66598-112">Dirección de un puntero al objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="66598-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66598-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66598-113">Return value</span></span>

<span data-ttu-id="66598-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66598-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66598-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="66598-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="66598-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="66598-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="66598-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66598-117">Remarks</span></span>

<span data-ttu-id="66598-118">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="66598-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="66598-119">Si se define Unicode, la llamada de función se resuelve como D3DXLoadPRTCompBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="66598-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="66598-120">De lo contrario, la llamada de función se resuelve como D3DXLoadPRTCompBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="66598-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="66598-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66598-121">Requirements</span></span>



| <span data-ttu-id="66598-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66598-122">Requirement</span></span> | <span data-ttu-id="66598-123">Value</span><span class="sxs-lookup"><span data-stu-id="66598-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66598-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66598-124">Header</span></span><br/>  | <dl> <span data-ttu-id="66598-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="66598-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="66598-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66598-126">Library</span></span><br/> | <dl> <span data-ttu-id="66598-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66598-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66598-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="66598-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66598-129">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="66598-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
