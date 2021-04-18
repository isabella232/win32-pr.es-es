---
title: Windows Numerics y las API de interoperabilidad de DirectXMath (Windowsnumerics. h)
description: Estas funciones convierten los tipos Windows. Foundation. Numerics a y desde los tipos SIMD de DirectXMath XMVECTOR y XMMATRIX.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Windows numéricos y API de interoperabilidad de DirectXMath
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721607"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="ec364-104">Windows numéricos y API de interoperabilidad de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ec364-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="ec364-105">Estas funciones convierten los tipos [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) a y desde los tipos SIMD de DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) y [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="ec364-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="ec364-106">Functions</span><span class="sxs-lookup"><span data-stu-id="ec364-106">Functions</span></span>

| <span data-ttu-id="ec364-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec364-107">Name</span></span> | <span data-ttu-id="ec364-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec364-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="ec364-109">Carga un float2 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="ec364-110">Carga un float3 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="ec364-111">Carga un FLOAT4 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="ec364-112">Carga un float3x2 en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="ec364-113">Carga un float4x4 en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="ec364-114">Carga un plano en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="ec364-115">Carga un cuaternión en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="ec364-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="ec364-116">Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un float2.</span><span class="sxs-lookup"><span data-stu-id="ec364-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="ec364-117">Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un float3.</span><span class="sxs-lookup"><span data-stu-id="ec364-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="ec364-118">Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en una FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="ec364-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="ec364-119">Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en un float3x2.</span><span class="sxs-lookup"><span data-stu-id="ec364-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="ec364-120">Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en un float4x4.</span><span class="sxs-lookup"><span data-stu-id="ec364-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="ec364-121">Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un plano.</span><span class="sxs-lookup"><span data-stu-id="ec364-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="ec364-122">Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="ec364-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ec364-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec364-123">Requirements</span></span>

| <span data-ttu-id="ec364-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec364-124">Requirement</span></span> | <span data-ttu-id="ec364-125">Value</span><span class="sxs-lookup"><span data-stu-id="ec364-125">Value</span></span> |
|-|-|
| <span data-ttu-id="ec364-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ec364-126">Namespace</span></span> | <span data-ttu-id="ec364-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="ec364-127">DirectX</span></span> |
| <span data-ttu-id="ec364-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec364-128">Header</span></span> | <dl> <span data-ttu-id="ec364-129"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec364-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ec364-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec364-130">See also</span></span>

[<span data-ttu-id="ec364-131">API de windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="ec364-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
