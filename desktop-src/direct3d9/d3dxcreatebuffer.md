---
description: Crea un objeto de búfer.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: Función D3DXCreateBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721541"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="5d089-103">D3DXCreateBuffer función)</span><span class="sxs-lookup"><span data-stu-id="5d089-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="5d089-104">Crea un objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="5d089-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d089-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d089-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5d089-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d089-107">*Numbytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d089-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d089-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d089-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d089-109">Tamaño del búfer que se va a crear, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5d089-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5d089-110">*ppBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d089-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d089-111">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d089-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5d089-112">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) que representa el objeto de búfer creado.</span><span class="sxs-lookup"><span data-stu-id="5d089-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d089-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d089-113">Return value</span></span>

<span data-ttu-id="5d089-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d089-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d089-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5d089-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5d089-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5d089-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d089-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d089-117">Requirements</span></span>



| <span data-ttu-id="5d089-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d089-118">Requirement</span></span> | <span data-ttu-id="5d089-119">Value</span><span class="sxs-lookup"><span data-stu-id="5d089-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d089-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d089-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5d089-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d089-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5d089-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d089-122">Library</span></span><br/> | <dl> <span data-ttu-id="5d089-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d089-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d089-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d089-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d089-125">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="5d089-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
