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
# <a name="directxmath"></a><span data-ttu-id="9e045-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9e045-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="9e045-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="9e045-104">Purpose</span></span>

<span data-ttu-id="9e045-105">La API de DirectXMath proporciona tipos y funciones de C++ compatibles con SIMD para las operaciones matemáticas de gráficos y álgebra lineal comunes comunes a las aplicaciones de DirectX.</span><span class="sxs-lookup"><span data-stu-id="9e045-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="9e045-106">La biblioteca proporciona versiones optimizadas para Windows 32-bit (x86), Windows 64 bits (x64) y Windows en ARM/ARM64 a través de la compatibilidad de intrínsecos SSE, AVX y ARM-neón en el compilador de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9e045-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="9e045-107">Para los desarrolladores que no están familiarizados con DirectXMath, considere la posibilidad de usar el contenedor SimpleMath en el *Kit de herramientas de DirectX* para [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="9e045-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e045-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9e045-108">In this section</span></span>



| <span data-ttu-id="9e045-109">Tema</span><span class="sxs-lookup"><span data-stu-id="9e045-109">Topic</span></span>                                                                     | <span data-ttu-id="9e045-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e045-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9e045-111">Guía de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9e045-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="9e045-112">DirectXMath proporciona una solución matemática optimizada para Windows.</span><span class="sxs-lookup"><span data-stu-id="9e045-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="9e045-113">Referencia de programación de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9e045-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="9e045-114">Esta sección contiene material de referencia para la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="9e045-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="9e045-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="9e045-115">Developer audience</span></span>

<span data-ttu-id="9e045-116">La biblioteca de DirectXMath está diseñada para desarrolladores de C++ que trabajan en juegos y gráficos de DirectX en aplicaciones de la tienda Windows, juegos de Xbox y aplicaciones de escritorio tradicionales para Windows.</span><span class="sxs-lookup"><span data-stu-id="9e045-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="9e045-117">Obtención de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9e045-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="9e045-118">Los encabezados de DirectXMath se distribuyen en el Windows SDK que viene con Visual Studio 2012 o posterior, y como un encabezado en línea, no hay ninguna biblioteca DLL o estática con la que vincular.</span><span class="sxs-lookup"><span data-stu-id="9e045-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="9e045-119">También está disponible como un paquete en [NuGet](https://www.nuget.org/packages/directxmath/).</span><span class="sxs-lookup"><span data-stu-id="9e045-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="9e045-120">DirectXMath es código abierto bajo la [licencia MIT](https://opensource.org/licenses/MIT) hospedada en [GitHub](https://github.com/Microsoft/DirectXMath).</span><span class="sxs-lookup"><span data-stu-id="9e045-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




