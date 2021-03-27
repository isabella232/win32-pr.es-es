---
title: outputtopology
description: Define el tipo primitivo de salida para del teselador.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994833"
---
# <a name="outputtopology"></a><span data-ttu-id="b7001-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="b7001-103">outputtopology</span></span>

<span data-ttu-id="b7001-104">Define el tipo primitivo de salida para del teselador.</span><span class="sxs-lookup"><span data-stu-id="b7001-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="b7001-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7001-105">Remarks</span></span>

<span data-ttu-id="b7001-106">X debe ser [**punto**](dx-graphics-hlsl-geometry-shader.md), **línea**, **triángulo \_ CW** o **triángulo \_ CCW** y debe incluirse entre comillas.</span><span class="sxs-lookup"><span data-stu-id="b7001-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="b7001-107">Estas son las opciones válidas para este atributo:</span><span class="sxs-lookup"><span data-stu-id="b7001-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="b7001-108">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b7001-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b7001-109">Vértice</span><span class="sxs-lookup"><span data-stu-id="b7001-109">Vertex</span></span> | <span data-ttu-id="b7001-110">Casco</span><span class="sxs-lookup"><span data-stu-id="b7001-110">Hull</span></span> | <span data-ttu-id="b7001-111">Dominio</span><span class="sxs-lookup"><span data-stu-id="b7001-111">Domain</span></span> | <span data-ttu-id="b7001-112">Geometría</span><span class="sxs-lookup"><span data-stu-id="b7001-112">Geometry</span></span> | <span data-ttu-id="b7001-113">Píxel</span><span class="sxs-lookup"><span data-stu-id="b7001-113">Pixel</span></span> | <span data-ttu-id="b7001-114">Compute</span><span class="sxs-lookup"><span data-stu-id="b7001-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b7001-115">x</span><span class="sxs-lookup"><span data-stu-id="b7001-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="b7001-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7001-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7001-117">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b7001-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7001-118">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b7001-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




