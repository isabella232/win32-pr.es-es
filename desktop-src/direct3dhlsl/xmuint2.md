---
title: Estructura XMUINT2
description: Describe un vector entero 2D sin signo.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- HLSL de la estructura XMUINT2
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549570"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="ea718-104">Estructura XMUINT2</span><span class="sxs-lookup"><span data-stu-id="ea718-104">XMUINT2 structure</span></span>

<span data-ttu-id="ea718-105">Describe un vector entero 2D sin signo.</span><span class="sxs-lookup"><span data-stu-id="ea718-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea718-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea718-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="ea718-107">Members</span><span class="sxs-lookup"><span data-stu-id="ea718-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea718-108">**x**</span><span class="sxs-lookup"><span data-stu-id="ea718-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="ea718-109">Componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="ea718-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="ea718-110">**y**</span><span class="sxs-lookup"><span data-stu-id="ea718-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="ea718-111">Componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="ea718-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="ea718-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea718-112">Remarks</span></span>

<span data-ttu-id="ea718-113">Esta estructura se define en el encabezado del ``D3DX\_DXGIFormatConvert.inl`` SDK de DirectX (junio de 2010) para su uso desde C++.</span><span class="sxs-lookup"><span data-stu-id="ea718-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="ea718-114">La versión más reciente de este encabezado en el paquete NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) en DirectXMath en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ea718-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="ea718-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea718-115">Requirements</span></span>



| <span data-ttu-id="ea718-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea718-116">Requirement</span></span> | <span data-ttu-id="ea718-117">Value</span><span class="sxs-lookup"><span data-stu-id="ea718-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea718-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea718-118">Header</span></span><br/> | <dl> <span data-ttu-id="ea718-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="ea718-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea718-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea718-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea718-121">Estructuras</span><span class="sxs-lookup"><span data-stu-id="ea718-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="ea718-122">Desempaquetar y empaquetar DXGI \_ FORMAT para In-Place de imágenes</span><span class="sxs-lookup"><span data-stu-id="ea718-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>