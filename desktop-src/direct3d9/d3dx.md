---
description: D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360041"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="827b8-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827b8-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="827b8-105">D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D.</span><span class="sxs-lookup"><span data-stu-id="827b8-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="827b8-106">D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="827b8-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="827b8-107">En esta versión del SDK de DirectX, solo se proporciona una versión de D3DX.</span><span class="sxs-lookup"><span data-stu-id="827b8-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="827b8-108">El archivo DLL de D3DX comercial se incluye en el redistribuible proporcionado en el SDK y se instala automáticamente como parte de la [instalación de DirectX con DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="827b8-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="827b8-109">La biblioteca de D3DX incluida en esta versión depende de los tiempos de ejecución de Direct3D que se incluyen con este SDK.</span><span class="sxs-lookup"><span data-stu-id="827b8-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="827b8-110">Las aplicaciones que se vinculan a la versión de D3DX en esta versión también deben redistribuir el Runtime desde este SDK.</span><span class="sxs-lookup"><span data-stu-id="827b8-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="827b8-111">Varias versiones de D3DX pueden residir de forma independiente en un único sistema simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="827b8-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="827b8-112">Al vincular estáticamente una aplicación a D3dx9. lib, la aplicación se vincula dinámicamente a la DLL de la versión de lanzamiento correspondiente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="827b8-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="827b8-113">Este archivo DLL corresponde a los encabezados de D3DX en los que se compila la aplicación (denominados con la \_ \_ constante versión del SDK de D3dx en D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="827b8-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="827b8-114">A medida que se publiquen nuevas versiones de D3DX en versiones futuras del SDK de DirectX, las aplicaciones que se vinculan a bibliotecas de D3DX anteriores permanecerán inalteradas.</span><span class="sxs-lookup"><span data-stu-id="827b8-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="827b8-115">La biblioteca de D3DX aborda estas áreas generales de funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="827b8-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="827b8-116">Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827b8-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="827b8-117">Compatibilidad de malla en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827b8-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="827b8-118">Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827b8-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="827b8-119">Compatibilidad con texturas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="827b8-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="827b8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="827b8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827b8-121">Introducción</span><span class="sxs-lookup"><span data-stu-id="827b8-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



