---
title: Estructura XMINT2
description: Describe un vector entero 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- HLSL de la estructura XMINT2
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222863"
---
# <a name="xmint2-structure"></a><span data-ttu-id="047aa-104">Estructura XMINT2</span><span class="sxs-lookup"><span data-stu-id="047aa-104">XMINT2 structure</span></span>

<span data-ttu-id="047aa-105">Describe un vector entero 2D.</span><span class="sxs-lookup"><span data-stu-id="047aa-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="047aa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="047aa-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="047aa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="047aa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="047aa-108">**x**</span><span class="sxs-lookup"><span data-stu-id="047aa-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="047aa-109">componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="047aa-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="047aa-110">**y**</span><span class="sxs-lookup"><span data-stu-id="047aa-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="047aa-111">componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="047aa-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="047aa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="047aa-112">Remarks</span></span>

<span data-ttu-id="047aa-113">Esta estructura se define en el ``D3DX\_DXGIFormatConvert.inl`` encabezado del SDK de DirectX (2010 de junio) para su uso desde C++.</span><span class="sxs-lookup"><span data-stu-id="047aa-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="047aa-114">La versión más reciente de este encabezado en el paquete NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) en DirectXMath en su lugar.</span><span class="sxs-lookup"><span data-stu-id="047aa-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="047aa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="047aa-115">Requirements</span></span>



| <span data-ttu-id="047aa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="047aa-116">Requirement</span></span> | <span data-ttu-id="047aa-117">Value</span><span class="sxs-lookup"><span data-stu-id="047aa-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047aa-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="047aa-118">Header</span></span><br/> | <dl> <span data-ttu-id="047aa-119"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="047aa-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047aa-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="047aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047aa-121">Estructuras</span><span class="sxs-lookup"><span data-stu-id="047aa-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="047aa-122">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="047aa-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
