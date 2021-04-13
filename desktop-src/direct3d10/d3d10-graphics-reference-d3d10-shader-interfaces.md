---
description: 'Esta sección contiene información sobre las siguientes interfaces del sombreador:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces del sombreador (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496301"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="242a9-103">Interfaces del sombreador (gráficos de Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="242a9-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="242a9-104">Esta sección contiene información sobre las siguientes interfaces del sombreador:</span><span class="sxs-lookup"><span data-stu-id="242a9-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="242a9-105">Cada una de estas interfaces de sombreador administra un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="242a9-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="242a9-106">La interfaz se crea cuando se compila un sombreador y, a continuación, se pasa a varias API que necesitan acceso a un sombreador compilado; por ejemplo, al enlazar un sombreador a una fase de canalización u obtener una firma de sombreador.</span><span class="sxs-lookup"><span data-stu-id="242a9-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="242a9-107">Interfaces de Pipeline-Stage</span><span class="sxs-lookup"><span data-stu-id="242a9-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="242a9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="242a9-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="242a9-109">**Interfaz ID3D10GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="242a9-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="242a9-110">Un sombreador de geometría implementa el procesamiento por primitivo en la [fase del sombreador de geometría](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="242a9-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="242a9-111">**Interfaz ID3D10PixelShader**</span><span class="sxs-lookup"><span data-stu-id="242a9-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="242a9-112">Un sombreador de píxeles implementa el procesamiento por píxel en la [fase del sombreador de píxeles](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="242a9-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="242a9-113">**Interfaz ID3D10VertexShader**</span><span class="sxs-lookup"><span data-stu-id="242a9-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="242a9-114">Un sombreador de vértices implementa el procesamiento por vértices en la [fase del sombreador de vértices](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="242a9-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="242a9-115">Las interfaces de reflexión del sombreador permiten a una aplicación inspeccionar el contenido de un sombreador en tiempo de diseño o de autor.</span><span class="sxs-lookup"><span data-stu-id="242a9-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="242a9-116">La reflexión del sombreador no es útil para establecer variables en tiempo de ejecución, ya que es un reflejo de los datos del sombreador y, por tanto, no admite ningún método para configurar los datos.</span><span class="sxs-lookup"><span data-stu-id="242a9-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="242a9-117">Interfaces de Shader-Reflection</span><span class="sxs-lookup"><span data-stu-id="242a9-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="242a9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="242a9-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="242a9-119">**Interfaz ID3D10ShaderReflection**</span><span class="sxs-lookup"><span data-stu-id="242a9-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="242a9-120">Una interfaz COM para leer información de un sombreador compilado en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="242a9-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="242a9-121">**Interfaz ID3D10ShaderReflectionConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="242a9-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="242a9-122">Una interfaz auxiliar para obtener una interfaz de búfer de constantes de reflexión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="242a9-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="242a9-123">**Interfaz ID3D10ShaderReflectionType**</span><span class="sxs-lookup"><span data-stu-id="242a9-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="242a9-124">Una interfaz auxiliar para obtener una interfaz de tipo de reflexión de sombreador.</span><span class="sxs-lookup"><span data-stu-id="242a9-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="242a9-125">**Interfaz ID3D10ShaderReflectionVariable**</span><span class="sxs-lookup"><span data-stu-id="242a9-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="242a9-126">Una interfaz auxiliar para obtener una interfaz del sombreador-reflexión-variable.</span><span class="sxs-lookup"><span data-stu-id="242a9-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="242a9-127">**Interfaz ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="242a9-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="242a9-128">Una interfaz de reflexión del sombreador para leer información de una vista de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="242a9-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="242a9-129">Las API de reflexión del sombreador implementan una interfaz de reflexión del sombreador COM ([**interfaz ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) y varias interfaces auxiliares que no son com (el resto de las interfaces).</span><span class="sxs-lookup"><span data-stu-id="242a9-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="242a9-130">La **interfaz ID3D10ShaderReflection** se crea cuando se crea un objeto de reflexión de sombreador.</span><span class="sxs-lookup"><span data-stu-id="242a9-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="242a9-131">Sigue las reglas estándar de COM; al crear la interfaz, se incrementa un recuento de referencias y la interfaz debe liberarse cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="242a9-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="242a9-132">Las interfaces restantes de reflexión del sombreador son interfaces auxiliares que no heredan de IUnknown.</span><span class="sxs-lookup"><span data-stu-id="242a9-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="242a9-133">Esto significa que no cambian ningún recuento de referencias cuando se crean y no es necesario que se destruyan cuando haya terminado con ellos.</span><span class="sxs-lookup"><span data-stu-id="242a9-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="242a9-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="242a9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="242a9-135">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="242a9-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
