---
title: API de windowsnumerics.h
description: El archivo de encabezado windowsnumerics.h define los tipos de vector y matriz de C++ en el Windows. Espacio de nombres Foundation.Numerics. Extiende los structs de Windows. Foundation.Numerics con una variedad de operadores matemáticos y funciones.
ms.assetid: 7aa15f80-c440-4dcb-a9a6-f1000a3a95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9caa0dfee7876095bd76c147fad3cd863c92ebcb90d96842a266a9a980f526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825195"
---
# <a name="windowsnumericsh-apis"></a>API de windowsnumerics.h

El archivo de encabezado windowsnumerics.h define los tipos de vector y matriz de C++ en [**el Windows. Espacio de nombres Foundation.Numerics.**](/uwp/api/Windows.Foundation.Numerics) Extiende los structs desde **Windows. Foundation.Numerics con** una variedad de operadores matemáticos y funciones.

Este espacio de nombres solo está disponible en C++. Su equivalente de .NET [es System.Numerics.](/dotnet/api/system.numerics?view=netframework-4.8)

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**float2 (estructura)**](float2-structure.md) | Vector con dos componentes. |
| [**float3 (estructura)**](float3-structure.md) | Vector con tres componentes. |
| [**float3x2 (estructura)**](float3x2-structure.md) | Matriz 3x2, que se usa para transformaciones 2D. |
| [**float4 (estructura)**](float4-structure.md) | Vector con cuatro componentes. |
| [**float4x4 (estructura)**](float4x4-structure.md) | Matriz 4x4, que se usa para transformaciones 3D. |
| [**estructura del plano**](plane-structure.md) | Esta estructura representa un plano mediante un vector 3D normal y un valor de distancia. |
| [**estructura de cuaternión**](quaternion-structure.md) | Vector de cuatro dimensiones, que se usa para representar una rotación. |
| [**Windows numéricas y las API de interoperabilidad de DirectXMath**](windows-numerics-and-directxmath-interop-apis.md) | Estas funciones convierten [**Windows. Tipos Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) hacia y desde los tipos SIMD de DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) y [XMMATRIX.](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |