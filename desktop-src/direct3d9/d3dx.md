---
description: D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D. D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910244"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="fec8b-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fec8b-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="fec8b-105">La biblioteca D3DX está en desuso.</span><span class="sxs-lookup"><span data-stu-id="fec8b-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="fec8b-106">Si la actualización a una versión más reciente de Direct3D y el código de utilidad asociado no es una opción, puede usar el paquete NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) en lugar de confiar en el SDK de DirectX heredado o DirectSetup.</span><span class="sxs-lookup"><span data-stu-id="fec8b-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="fec8b-107">D3DX es una biblioteca de herramientas diseñada para proporcionar funcionalidad de gráficos adicional sobre Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fec8b-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="fec8b-108">D3DX se proporciona como una biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="fec8b-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="fec8b-109">Solo se proporciona una versión de D3DX en esta versión del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="fec8b-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="fec8b-110">El archivo DLL D3DX comercial se incluye en el redistribuible proporcionado en el SDK y se instala automáticamente como parte de la instalación de **DirectX con DirectSetup.**</span><span class="sxs-lookup"><span data-stu-id="fec8b-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="fec8b-111">La biblioteca D3DX incluida en esta versión depende de los entornos de ejecución de Direct3D que se incluyen con este SDK.</span><span class="sxs-lookup"><span data-stu-id="fec8b-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="fec8b-112">Las aplicaciones que se vinculan con la versión de D3DX de esta versión también deben redistribuir el entorno de ejecución de este SDK.</span><span class="sxs-lookup"><span data-stu-id="fec8b-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="fec8b-113">Varias versiones de D3DX pueden residir de forma independiente en un único sistema simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="fec8b-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="fec8b-114">Al vincular estáticamente una aplicación a D3dx9.lib, la aplicación vincula dinámicamente al archivo DLL D3DX comercial correspondiente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="fec8b-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="fec8b-115">Este archivo DLL corresponde a los encabezados D3DX con los que se compila la aplicación (denominados con la constante VERSION del \_ SDK \_ D3DX en D3dx9core.h).</span><span class="sxs-lookup"><span data-stu-id="fec8b-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="fec8b-116">A medida que se envíen nuevas versiones de D3DX en futuras versiones del SDK de DirectX, las aplicaciones que se vinculen a bibliotecas D3DX anteriores no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="fec8b-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="fec8b-117">La biblioteca D3DX aborda estas áreas generales de funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="fec8b-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="fec8b-118">Compatibilidad con el dibujo de líneas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fec8b-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="fec8b-119">Compatibilidad con mallas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fec8b-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="fec8b-120">Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fec8b-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="fec8b-121">Compatibilidad con texturas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fec8b-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="fec8b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fec8b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fec8b-123">Introducción</span><span class="sxs-lookup"><span data-stu-id="fec8b-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



