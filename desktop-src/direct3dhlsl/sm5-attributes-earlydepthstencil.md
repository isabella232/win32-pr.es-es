---
title: earlydepthstencil
description: Fuerza la prueba de la galería de símbolos de profundidad antes de que se ejecute un sombreador.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996960"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="2aa0a-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="2aa0a-103">earlydepthstencil</span></span>

<span data-ttu-id="2aa0a-104">Fuerza la prueba de la galería de símbolos de profundidad antes de que se ejecute un sombreador.</span><span class="sxs-lookup"><span data-stu-id="2aa0a-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="2aa0a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2aa0a-105">Remarks</span></span>

<span data-ttu-id="2aa0a-106">La prueba de profundidad-estarcido normalmente se realiza durante el procesamiento de píxeles mediante un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2aa0a-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="2aa0a-107">Forzar la prueba temprana de la galería de símbolos hace que las pruebas se realicen antes de la ejecución del sombreador; el propósito es mejorar el rendimiento por píxel al reactivar o reducir/evitar el procesamiento de píxeles innecesario.</span><span class="sxs-lookup"><span data-stu-id="2aa0a-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="2aa0a-108">Una aplicación puede forzar la realización de pruebas tempranas de la galería de símbolos al proporcionar el atributo o el hardware puede ejecutar las pruebas de nivel de estarcido de nivel más rápido, siempre que no se escriban valores de profundidad y no se realicen operaciones de acceso no ordenado en un sombreador como una optimización.</span><span class="sxs-lookup"><span data-stu-id="2aa0a-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="2aa0a-109">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2aa0a-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2aa0a-110">Vértice</span><span class="sxs-lookup"><span data-stu-id="2aa0a-110">Vertex</span></span> | <span data-ttu-id="2aa0a-111">Casco</span><span class="sxs-lookup"><span data-stu-id="2aa0a-111">Hull</span></span> | <span data-ttu-id="2aa0a-112">Dominio</span><span class="sxs-lookup"><span data-stu-id="2aa0a-112">Domain</span></span> | <span data-ttu-id="2aa0a-113">Geometría</span><span class="sxs-lookup"><span data-stu-id="2aa0a-113">Geometry</span></span> | <span data-ttu-id="2aa0a-114">Píxel</span><span class="sxs-lookup"><span data-stu-id="2aa0a-114">Pixel</span></span> | <span data-ttu-id="2aa0a-115">Compute</span><span class="sxs-lookup"><span data-stu-id="2aa0a-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2aa0a-116">x</span><span class="sxs-lookup"><span data-stu-id="2aa0a-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="2aa0a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2aa0a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa0a-118">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2aa0a-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="2aa0a-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2aa0a-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




