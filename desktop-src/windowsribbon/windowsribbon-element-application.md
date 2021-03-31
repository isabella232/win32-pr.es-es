---
title: Elemento Application
description: Representa el elemento de nivel superior en la especificación de marcado del marco de la cinta de Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Cinta de opciones de Windows, elemento de aplicación
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103797187"
---
# <a name="application-element"></a><span data-ttu-id="a7324-104">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="a7324-104">Application element</span></span>

<span data-ttu-id="a7324-105">Representa el elemento de nivel superior en la especificación de marcado del marco de la cinta de Windows.</span><span class="sxs-lookup"><span data-stu-id="a7324-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="a7324-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a7324-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="a7324-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7324-107">Attributes</span></span>



| <span data-ttu-id="a7324-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a7324-108">Attribute</span></span>            | <span data-ttu-id="a7324-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7324-109">Type</span></span>                 | <span data-ttu-id="a7324-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a7324-110">Required</span></span>       | <span data-ttu-id="a7324-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7324-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7324-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="a7324-112">**xmlns**</span></span><br/> | <span data-ttu-id="a7324-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a7324-113">xs:string</span></span><br/> | <span data-ttu-id="a7324-114">Sí</span><span class="sxs-lookup"><span data-stu-id="a7324-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="a7324-115">El URI para el enlace del espacio de nombres de marcado de la cinta.</span><span class="sxs-lookup"><span data-stu-id="a7324-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="a7324-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7324-116">Child elements</span></span>



| <span data-ttu-id="a7324-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7324-117">Element</span></span>                                                                               | <span data-ttu-id="a7324-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7324-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="a7324-119">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="a7324-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="a7324-120">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="a7324-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="a7324-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="a7324-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="a7324-122">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="a7324-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a7324-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a7324-123">Parent elements</span></span>

<span data-ttu-id="a7324-124">No hay elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a7324-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7324-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7324-125">Remarks</span></span>

<span data-ttu-id="a7324-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7324-126">Required.</span></span>

<span data-ttu-id="a7324-127">Debe aparecer exactamente una vez como contenedor para todo el marcado de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="a7324-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="a7324-128">Los elementos secundarios del elemento **Application** deben aparecer en el orden especificado:</span><span class="sxs-lookup"><span data-stu-id="a7324-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="a7324-129">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="a7324-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="a7324-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="a7324-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="a7324-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a7324-131">Examples</span></span>

<span data-ttu-id="a7324-132">En el ejemplo siguiente se muestra una declaración de elemento de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="a7324-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="a7324-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a7324-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a7324-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7324-134">Minimum supported system</span></span><br/> | <span data-ttu-id="a7324-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7324-135">Windows 7</span></span> |
| <span data-ttu-id="a7324-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a7324-136">Can be empty</span></span>                        | <span data-ttu-id="a7324-137">No</span><span class="sxs-lookup"><span data-stu-id="a7324-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="a7324-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a7324-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7324-139">Declarar comandos y controles con el marcado de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="a7324-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





