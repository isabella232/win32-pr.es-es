---
title: Windows numéricos y las API de interoperabilidad de DirectXMath (Windowsnumerics.h)
description: Estas funciones convierten Windows. Tipos Foundation.Numerics hacia y desde los tipos SIMD de DirectXMath XMVECTOR y XMMATRIX.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Windows numéricos y las API de interoperabilidad de DirectXMath
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
ms.openlocfilehash: f4b84a67dfa239647ae14530d8d1b4185f340df3df98afb36a0b65c52fc5c5da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112845"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Windows numéricos y las API de interoperabilidad de DirectXMath

Estas funciones convierten [**Windows. Tipos Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) hacia y desde los tipos SIMD de DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) y [XMMATRIX.](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)

## <a name="functions"></a>Funciones

| Nombre | Descripción |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Carga un valor float2 en un [XMVECTOR de](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Carga un valor float3 en un [XMVECTOR de](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Carga un valor float4 en un [XMVECTOR de](../dxmath/xmvector-data-type.md)DirectXMath. |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Carga un float3x2 en un [XMMATRIX de](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Carga un float4x4 en un [XMMATRIX de](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Carga un plano en un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)de DirectXMath. |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Carga un cuaternión en un [XMMATRIX de](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)DirectXMath. |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en float4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Almacena un [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) de DirectXMath en float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un plano. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Almacena un [XMVECTOR](../dxmath/xmvector-data-type.md) de DirectXMath en un cuaternión. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Espacio de nombres | DirectX |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[API de windowsnumerics.h](windowsnumerics-h-apis-portal.md)
