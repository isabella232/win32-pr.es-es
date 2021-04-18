---
title: Raytracing estructuras HLSL (Direct3D 12)
description: Las siguientes estructuras HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "105720099"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="227f8-103">Raytracing estructuras HLSL (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="227f8-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="227f8-104">Las siguientes estructuras HLSL admiten la canalización raytracing de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="227f8-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="227f8-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="227f8-105">In this section</span></span>



| <span data-ttu-id="227f8-106">Tema</span><span class="sxs-lookup"><span data-stu-id="227f8-106">Topic</span></span>                                                                                                       | <span data-ttu-id="227f8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="227f8-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="227f8-108">**Estructura del parámetro de llamadas**</span><span class="sxs-lookup"><span data-stu-id="227f8-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="227f8-109">Una estructura definida por el usuario que se proporciona como un argumento INOUT a una llamada a CallShader y como un parámetro INOUT para el sombreador al que se puede llamar.</span><span class="sxs-lookup"><span data-stu-id="227f8-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="227f8-110">**Estructura de atributos de intersección**</span><span class="sxs-lookup"><span data-stu-id="227f8-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="227f8-111">Una estructura definida por el usuario que se proporciona como un argumento INOUT en una llamada [**TraceRay**](traceray-function.md) y como un parámetro INOUT en los tipos de sombreador que pueden tener acceso a la carga de rayo.</span><span class="sxs-lookup"><span data-stu-id="227f8-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="227f8-112">**Estructura de la carga de rayos**</span><span class="sxs-lookup"><span data-stu-id="227f8-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="227f8-113">Una estructura definida por el usuario que se proporciona como un argumento INOUT en una llamada [**TraceRay**](traceray-function.md) y como un parámetro INOUT en los tipos de sombreador que pueden tener acceso a la carga de rayo.</span><span class="sxs-lookup"><span data-stu-id="227f8-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="227f8-114">**Estructura RayDesc**</span><span class="sxs-lookup"><span data-stu-id="227f8-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="227f8-115">Marcas que se pasan a la función [**TraceRay**](traceray-function.md) para invalidar la transparencia, la selección y el comportamiento de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="227f8-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="227f8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="227f8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="227f8-117">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="227f8-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="227f8-118">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="227f8-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





