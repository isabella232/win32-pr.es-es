---
description: Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995862"
---
# <a name="faultinfo-element"></a><span data-ttu-id="87251-103">elemento faultInfo</span><span class="sxs-lookup"><span data-stu-id="87251-103">faultInfo element</span></span>

<span data-ttu-id="87251-104">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="87251-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="87251-105">Uso</span><span class="sxs-lookup"><span data-stu-id="87251-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="87251-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="87251-106">Attributes</span></span>

<span data-ttu-id="87251-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="87251-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="87251-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87251-108">Child elements</span></span>

<span data-ttu-id="87251-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="87251-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="87251-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="87251-110">Parent elements</span></span>



| <span data-ttu-id="87251-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="87251-111">Element</span></span>                                                                         | <span data-ttu-id="87251-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="87251-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87251-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="87251-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="87251-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="87251-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="87251-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="87251-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="87251-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="87251-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="87251-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="87251-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="87251-118">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="87251-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="87251-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="87251-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="87251-120">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="87251-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="87251-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87251-121">Remarks</span></span>

<span data-ttu-id="87251-122">Los valores posibles son 1 (parámetros de error incluidos) y 0 (parámetros de error excluidos).</span><span class="sxs-lookup"><span data-stu-id="87251-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="87251-123">De forma predeterminada, se excluyen los parámetros de error.</span><span class="sxs-lookup"><span data-stu-id="87251-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="87251-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="87251-124">Element information</span></span>



| <span data-ttu-id="87251-125">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="87251-125">Label</span></span> | <span data-ttu-id="87251-126">Value</span><span class="sxs-lookup"><span data-stu-id="87251-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="87251-127">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87251-127">Minimum supported system</span></span><br/> | <span data-ttu-id="87251-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87251-128">Windows Vista</span></span> |
| <span data-ttu-id="87251-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="87251-129">Can be empty</span></span>                        | <span data-ttu-id="87251-130">Sí</span><span class="sxs-lookup"><span data-stu-id="87251-130">Yes</span></span>           |



 

 




