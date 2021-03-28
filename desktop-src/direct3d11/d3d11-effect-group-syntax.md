---
title: Sintaxis de grupo de efectos (Direct3D 11)
description: Un grupo de efectos se declara con la sintaxis descrita en esta sección.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104487186"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="88bf5-103">Sintaxis de grupo de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="88bf5-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="88bf5-104">Un grupo de efectos se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="88bf5-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="88bf5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88bf5-105">Parameters</span></span>



| <span data-ttu-id="88bf5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="88bf5-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="88bf5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="88bf5-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88bf5-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="88bf5-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="88bf5-109">palabra clave ecesario.</span><span class="sxs-lookup"><span data-stu-id="88bf5-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="88bf5-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="88bf5-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="88bf5-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88bf5-111">Required.</span></span> <span data-ttu-id="88bf5-112">Cadena ASCII que identifica de forma única el nombre del grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="88bf5-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="88bf5-113">A diferencia de las técnicas, los grupos deben tener nombres para asegurarse de que las técnicas tienen un identificador único (consulte la sección grupos y técnicas a continuación).</span><span class="sxs-lookup"><span data-stu-id="88bf5-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="88bf5-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < anotaciones ></span><span class="sxs-lookup"><span data-stu-id="88bf5-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="88bf5-115">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="88bf5-115">\[in\] Optional.</span></span> <span data-ttu-id="88bf5-116">Una o más partes de la información proporcionada por el usuario (metadatos) que el sistema de efectos omite.</span><span class="sxs-lookup"><span data-stu-id="88bf5-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="88bf5-117">Para ver la sintaxis, vea sintaxis de anotación (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="88bf5-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="88bf5-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="88bf5-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="88bf5-119">"Technique10" o "technique11".</span><span class="sxs-lookup"><span data-stu-id="88bf5-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="88bf5-120">Las técnicas que usan la funcionalidad nueva en Direct3D 11 (5 \_ 0 sombreadores, BindInterfaces, etc.) deben usar "technique11".</span><span class="sxs-lookup"><span data-stu-id="88bf5-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="88bf5-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span><span class="sxs-lookup"><span data-stu-id="88bf5-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="88bf5-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="88bf5-122">Optional.</span></span> <span data-ttu-id="88bf5-123">Cadena ASCII que identifica de forma única el nombre de la técnica de efecto.</span><span class="sxs-lookup"><span data-stu-id="88bf5-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="88bf5-124">Grupos y técnicas</span><span class="sxs-lookup"><span data-stu-id="88bf5-124">Groups and Techniques</span></span>

<span data-ttu-id="88bf5-125">Para mantener la compatibilidad con efectos de FX \_ 4 \_ 0, los grupos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="88bf5-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="88bf5-126">Hay un grupo de nombres NULL implícito que rodea todas las técnicas globales.</span><span class="sxs-lookup"><span data-stu-id="88bf5-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="88bf5-127">Considere el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="88bf5-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="88bf5-128">En C++, se puede obtener una técnica por nombre de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="88bf5-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="88bf5-129">Los siguientes comandos encontrarán las técnicas obvias:</span><span class="sxs-lookup"><span data-stu-id="88bf5-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="88bf5-130">Para asegurarse de que [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funciona de forma similar a los efectos 10, todos los grupos definidos deben tener un nombre.</span><span class="sxs-lookup"><span data-stu-id="88bf5-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88bf5-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88bf5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88bf5-132">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="88bf5-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="88bf5-133">Sintaxis de la técnica de efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="88bf5-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





