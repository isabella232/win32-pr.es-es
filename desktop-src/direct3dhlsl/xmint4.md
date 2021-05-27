---
title: Estructura XMINT4
description: Describe un vector entero 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL de estructura XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549960"
---
# <a name="xmint4-structure"></a><span data-ttu-id="abeb5-104">Estructura XMINT4</span><span class="sxs-lookup"><span data-stu-id="abeb5-104">XMINT4 structure</span></span>

<span data-ttu-id="abeb5-105">Describe un vector entero 4D.</span><span class="sxs-lookup"><span data-stu-id="abeb5-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="abeb5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abeb5-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="abeb5-107">Members</span><span class="sxs-lookup"><span data-stu-id="abeb5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="abeb5-108">**x**</span><span class="sxs-lookup"><span data-stu-id="abeb5-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="abeb5-109">Componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="abeb5-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="abeb5-110">**y**</span><span class="sxs-lookup"><span data-stu-id="abeb5-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="abeb5-111">Componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="abeb5-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="abeb5-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="abeb5-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="abeb5-113">Componente z del vector.</span><span class="sxs-lookup"><span data-stu-id="abeb5-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="abeb5-114">**w**</span><span class="sxs-lookup"><span data-stu-id="abeb5-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="abeb5-115">w-component del vector.</span><span class="sxs-lookup"><span data-stu-id="abeb5-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abeb5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abeb5-116">Requirements</span></span>



| <span data-ttu-id="abeb5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="abeb5-117">Requirement</span></span> | <span data-ttu-id="abeb5-118">Value</span><span class="sxs-lookup"><span data-stu-id="abeb5-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abeb5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abeb5-119">Header</span></span><br/> | <dl> <span data-ttu-id="abeb5-120"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="abeb5-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="abeb5-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abeb5-121">Remarks</span></span>

<span data-ttu-id="abeb5-122">Esta estructura se define en el encabezado ``D3DX\_DXGIFormatConvert.inl`` del SDK de DirectX (junio de 2010) para su uso desde C++.</span><span class="sxs-lookup"><span data-stu-id="abeb5-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="abeb5-123">La versión más reciente de este encabezado en el paquete NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) en DirectXMath en su lugar.</span><span class="sxs-lookup"><span data-stu-id="abeb5-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="abeb5-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="abeb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abeb5-125">Estructuras</span><span class="sxs-lookup"><span data-stu-id="abeb5-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="abeb5-126">Desempaquetar y empaquetar DXGI \_ FORMAT para In-Place de imágenes</span><span class="sxs-lookup"><span data-stu-id="abeb5-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>