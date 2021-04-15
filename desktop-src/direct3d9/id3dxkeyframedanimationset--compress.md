---
description: Transforma las animaciones de una animación establecida en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Método ID3DXKeyframedAnimationSet:: compress (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708078"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="776b2-103">ID3DXKeyframedAnimationSet:: compress (método)</span><span class="sxs-lookup"><span data-stu-id="776b2-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="776b2-104">Transforma las animaciones de una animación establecida en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="776b2-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="776b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="776b2-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="776b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="776b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776b2-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="776b2-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776b2-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="776b2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="776b2-109">Uno de los valores de las [**\_ marcas D3DXCOMPRESSION**](./d3dxcompression-flags.md) que definen el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos.</span><span class="sxs-lookup"><span data-stu-id="776b2-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="776b2-110">D3DXCOMPRESS \_ default es el único valor que se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="776b2-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="776b2-111">*Disminución* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="776b2-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776b2-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="776b2-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="776b2-113">Proporción de pérdida de compresión deseada, en el intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="776b2-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="776b2-114">*pHierarchy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="776b2-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776b2-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="776b2-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="776b2-116">Puntero a una jerarquía de fotogramas de transformación [**D3DXFRAME**](d3dxframe.md) .</span><span class="sxs-lookup"><span data-stu-id="776b2-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="776b2-117">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="776b2-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="776b2-118">*ppCompressedData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="776b2-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="776b2-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="776b2-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="776b2-120">Dirección de un puntero al conjunto de animaciones comprimidas de [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="776b2-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776b2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="776b2-121">Return value</span></span>

<span data-ttu-id="776b2-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="776b2-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="776b2-123">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="776b2-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="776b2-124">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="776b2-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="776b2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="776b2-125">Requirements</span></span>



| <span data-ttu-id="776b2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="776b2-126">Requirement</span></span> | <span data-ttu-id="776b2-127">Value</span><span class="sxs-lookup"><span data-stu-id="776b2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="776b2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="776b2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="776b2-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="776b2-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="776b2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="776b2-130">Library</span></span><br/> | <dl> <span data-ttu-id="776b2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="776b2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="776b2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="776b2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776b2-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="776b2-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
