---
description: 'Esta sección contiene información sobre las siguientes funciones del sombreador:'
ms.assetid: c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32
title: Funciones del sombreador (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac0136eee8648512287eb146bbae02256fb223
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360065"
---
# <a name="shader-functions-direct3d-10-graphics"></a><span data-ttu-id="eec66-103">Funciones del sombreador (gráficos de Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="eec66-103">Shader Functions (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="eec66-104">Esta sección contiene información sobre las siguientes funciones del sombreador:</span><span class="sxs-lookup"><span data-stu-id="eec66-104">This section contains information about the following shader functions:</span></span>



| <span data-ttu-id="eec66-105">Functions</span><span class="sxs-lookup"><span data-stu-id="eec66-105">Functions</span></span>                                                                          | <span data-ttu-id="eec66-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec66-106">Description</span></span>                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="eec66-107">**D3D10CompileShader**</span><span class="sxs-lookup"><span data-stu-id="eec66-107">**D3D10CompileShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader)                                   | <span data-ttu-id="eec66-108">Compilar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec66-108">Compile a shader.</span></span>                                                           |
| [<span data-ttu-id="eec66-109">**D3D10DisassembleShader**</span><span class="sxs-lookup"><span data-stu-id="eec66-109">**D3D10DisassembleShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10disassembleshader)                           | <span data-ttu-id="eec66-110">En desuso.</span><span class="sxs-lookup"><span data-stu-id="eec66-110">Deprecated.</span></span> <span data-ttu-id="eec66-111">Vea [**D3DX10DisassembleShader**](d3dx10disassembleshader.md).</span><span class="sxs-lookup"><span data-stu-id="eec66-111">See [**D3DX10DisassembleShader**](d3dx10disassembleshader.md).</span></span> |
| [<span data-ttu-id="eec66-112">**D3D10GetGeometryShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="eec66-112">**D3D10GetGeometryShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getgeometryshaderprofile)             | <span data-ttu-id="eec66-113">Obtiene el perfil de sombreador de geometría más adecuado para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="eec66-113">Get the geometry-shader profile best suited to a given device.</span></span>              |
| [<span data-ttu-id="eec66-114">**D3D10GetInputAndOutputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="eec66-114">**D3D10GetInputAndOutputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getinputandoutputsignatureblob) | <span data-ttu-id="eec66-115">Obtiene un búfer que contiene las firmas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec66-115">Get a buffer that contains shader signatures.</span></span>                               |
| [<span data-ttu-id="eec66-116">**D3D10GetInputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="eec66-116">**D3D10GetInputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getinputsignatureblob)                   | <span data-ttu-id="eec66-117">Obtiene un búfer que contiene las firmas de entrada del sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec66-117">Get a buffer that contains shader input signatures.</span></span>                         |
| [<span data-ttu-id="eec66-118">**D3D10GetOutputSignatureBlob**</span><span class="sxs-lookup"><span data-stu-id="eec66-118">**D3D10GetOutputSignatureBlob**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getoutputsignatureblob)                 | <span data-ttu-id="eec66-119">Obtiene un búfer que contiene las firmas de salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec66-119">Get a buffer that contains shader output signatures.</span></span>                        |
| [<span data-ttu-id="eec66-120">**D3D10GetPixelShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="eec66-120">**D3D10GetPixelShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getpixelshaderprofile)                   | <span data-ttu-id="eec66-121">Obtiene el perfil de sombreador de píxeles más adecuado para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="eec66-121">Get the pixel-shader profile best suited to a given device.</span></span>                 |
| [<span data-ttu-id="eec66-122">**D3D10GetShaderDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="eec66-122">**D3D10GetShaderDebugInfo**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getshaderdebuginfo)                         | <span data-ttu-id="eec66-123">Obtiene la información de depuración del sombreador de un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="eec66-123">Get shader debug info from a compiled shader.</span></span>                               |
| [<span data-ttu-id="eec66-124">**D3D10GetVertexShaderProfile**</span><span class="sxs-lookup"><span data-stu-id="eec66-124">**D3D10GetVertexShaderProfile**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10getvertexshaderprofile)                 | <span data-ttu-id="eec66-125">Obtiene el perfil del sombreador de vértices más adecuado para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="eec66-125">Get the vertex-shader profile best suited to a given device.</span></span>                |
| [<span data-ttu-id="eec66-126">**D3D10PreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="eec66-126">**D3D10PreprocessShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10preprocessshader)                             | <span data-ttu-id="eec66-127">Genere una cadena de texto que contenga la secuencia del token del sombreador.</span><span class="sxs-lookup"><span data-stu-id="eec66-127">Generate a text string that contains the shader token stream.</span></span>               |
| [<span data-ttu-id="eec66-128">**D3D10ReflectShader**</span><span class="sxs-lookup"><span data-stu-id="eec66-128">**D3D10ReflectShader**</span></span>](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10reflectshader)                                   | <span data-ttu-id="eec66-129">En desuso.</span><span class="sxs-lookup"><span data-stu-id="eec66-129">Deprecated.</span></span> <span data-ttu-id="eec66-130">Vea [**D3DX10ReflectShader**](d3dx10reflectshader.md).</span><span class="sxs-lookup"><span data-stu-id="eec66-130">See [**D3DX10ReflectShader**](d3dx10reflectshader.md).</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="eec66-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eec66-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eec66-132">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="eec66-132">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 



