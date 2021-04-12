---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361999"
---
# <a name="directxmath"></a>DirectXMath

## <a name="purpose"></a>Propósito

La API de DirectXMath proporciona tipos y funciones de C++ compatibles con SIMD para las operaciones matemáticas de gráficos y álgebra lineal comunes comunes a las aplicaciones de DirectX. La biblioteca proporciona versiones optimizadas para Windows 32-bit (x86), Windows 64 bits (x64) y Windows en ARM/ARM64 a través de la compatibilidad de intrínsecos SSE, AVX y ARM-neón en el compilador de Visual C++.

Para los desarrolladores que no están familiarizados con DirectXMath, considere la posibilidad de usar el contenedor SimpleMath en el *Kit de herramientas de DirectX* para [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) como punto de partida.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Guía de programación de DirectXMath](ovw-xnamath-progguide.md)<br/>     | DirectXMath proporciona una solución matemática optimizada para Windows.<br/>           |
| [Referencia de programación de DirectXMath](ovw-xnamath-reference.md)<br/> | Esta sección contiene material de referencia para la biblioteca de DirectXMath.<br/> |



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La biblioteca de DirectXMath está diseñada para desarrolladores de C++ que trabajan en juegos y gráficos de DirectX en aplicaciones de la tienda Windows, juegos de Xbox y aplicaciones de escritorio tradicionales para Windows.

## <a name="obtaining-directxmath"></a>Obtención de DirectXMath
 
Los encabezados de DirectXMath se distribuyen en el Windows SDK que viene con Visual Studio 2012 o posterior, y como un encabezado en línea, no hay ninguna biblioteca DLL o estática con la que vincular. También está disponible como un paquete en [NuGet](https://www.nuget.org/packages/directxmath/).

DirectXMath es código abierto bajo la [licencia MIT](https://opensource.org/licenses/MIT) hospedada en [GitHub](https://github.com/Microsoft/DirectXMath).




