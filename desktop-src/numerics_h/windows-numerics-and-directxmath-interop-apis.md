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
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Windows numéricos y API de interoperabilidad de DirectXMath

Estas funciones convierten los tipos [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) a y desde los tipos SIMD de DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) y [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Functions

| Nombre | Descripción |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Carga un float2 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath. |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Carga un float3 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath. |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Carga un FLOAT4 en un [XMVECTOR](../dxmath/xmvector-data-type.md)de DirectXMath. |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Carga un float3x2 en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath. |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Carga un float4x4 en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath. |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Carga un plano en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath. |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Carga un cuaternión en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath. |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en una FLOAT4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en un float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en un float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un plano. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un cuaternión. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | DirectX |
| Encabezado | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics. h](windowsnumerics-h-apis-portal.md)
