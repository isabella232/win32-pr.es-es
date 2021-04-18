---
description: Recupera información sobre un archivo de imagen determinado en la memoria.
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: Función D3DXGetImageInfoFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718190"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="831bb-103">D3DXGetImageInfoFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="831bb-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="831bb-104">Recupera información sobre un archivo de imagen determinado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="831bb-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="831bb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="831bb-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="831bb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="831bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831bb-107">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="831bb-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bb-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="831bb-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="831bb-109">Puntero VOID al archivo de código fuente en la memoria.</span><span class="sxs-lookup"><span data-stu-id="831bb-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="831bb-110">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="831bb-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="831bb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="831bb-112">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="831bb-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="831bb-113">.</span><span class="sxs-lookup"><span data-stu-id="831bb-113">.</span></span>

</dd> <dt>

<span data-ttu-id="831bb-114">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="831bb-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bb-115">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="831bb-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="831bb-116">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con la descripción de los datos del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="831bb-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831bb-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="831bb-117">Return value</span></span>

<span data-ttu-id="831bb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="831bb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="831bb-119">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="831bb-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="831bb-120">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="831bb-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="831bb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="831bb-121">Requirements</span></span>



| <span data-ttu-id="831bb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="831bb-122">Requirement</span></span> | <span data-ttu-id="831bb-123">Value</span><span class="sxs-lookup"><span data-stu-id="831bb-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="831bb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="831bb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="831bb-125"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="831bb-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="831bb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="831bb-126">Library</span></span><br/> | <dl> <span data-ttu-id="831bb-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="831bb-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="831bb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="831bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831bb-129">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="831bb-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="831bb-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="831bb-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="831bb-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="831bb-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
