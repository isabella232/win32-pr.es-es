---
title: Estructura XMINT4
description: Describe un vector entero 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL de la estructura XMINT4
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
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222843"
---
# <a name="xmint4-structure"></a><span data-ttu-id="dea5e-104">Estructura XMINT4</span><span class="sxs-lookup"><span data-stu-id="dea5e-104">XMINT4 structure</span></span>

<span data-ttu-id="dea5e-105">Describe un vector entero 4D.</span><span class="sxs-lookup"><span data-stu-id="dea5e-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea5e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dea5e-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="dea5e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dea5e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dea5e-108">**x**</span><span class="sxs-lookup"><span data-stu-id="dea5e-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="dea5e-109">componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="dea5e-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="dea5e-110">**y**</span><span class="sxs-lookup"><span data-stu-id="dea5e-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="dea5e-111">componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="dea5e-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="dea5e-112">**z**</span><span class="sxs-lookup"><span data-stu-id="dea5e-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="dea5e-113">componente z del vector.</span><span class="sxs-lookup"><span data-stu-id="dea5e-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="dea5e-114">**w**</span><span class="sxs-lookup"><span data-stu-id="dea5e-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="dea5e-115">componente w del vector.</span><span class="sxs-lookup"><span data-stu-id="dea5e-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dea5e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea5e-116">Requirements</span></span>



| <span data-ttu-id="dea5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea5e-117">Requirement</span></span> | <span data-ttu-id="dea5e-118">Value</span><span class="sxs-lookup"><span data-stu-id="dea5e-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea5e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dea5e-119">Header</span></span><br/> | <dl> <span data-ttu-id="dea5e-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="dea5e-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="dea5e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dea5e-121">Remarks</span></span>

<span data-ttu-id="dea5e-122">Esta estructura se define en el ``D3DX\_DXGIFormatConvert.inl`` encabezado del SDK de DirectX (2010 de junio) para su uso desde C++.</span><span class="sxs-lookup"><span data-stu-id="dea5e-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="dea5e-123">La versión más reciente de este encabezado en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX:: XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) en DirectXMath en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dea5e-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="dea5e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dea5e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea5e-125">Estructuras</span><span class="sxs-lookup"><span data-stu-id="dea5e-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="dea5e-126">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="dea5e-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
