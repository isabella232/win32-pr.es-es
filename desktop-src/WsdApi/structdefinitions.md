---
description: Genera definiciones de estructura de C para los tipos conocidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706555"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="37e5e-103">elemento structDefinitions</span><span class="sxs-lookup"><span data-stu-id="37e5e-103">structDefinitions element</span></span>

<span data-ttu-id="37e5e-104">Genera definiciones de estructura de C para los tipos conocidos.</span><span class="sxs-lookup"><span data-stu-id="37e5e-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="37e5e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="37e5e-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="37e5e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="37e5e-106">Attributes</span></span>

<span data-ttu-id="37e5e-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="37e5e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="37e5e-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37e5e-108">Child elements</span></span>

<span data-ttu-id="37e5e-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="37e5e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="37e5e-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="37e5e-110">Parent elements</span></span>



| <span data-ttu-id="37e5e-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="37e5e-111">Element</span></span>                         | <span data-ttu-id="37e5e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="37e5e-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="37e5e-113">**archivo**</span><span class="sxs-lookup"><span data-stu-id="37e5e-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="37e5e-114">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="37e5e-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="37e5e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37e5e-115">Remarks</span></span>

<span data-ttu-id="37e5e-116">La mayoría del código generado y el código de aplicación hacen referencia a las estructuras de los tipos conocidos.</span><span class="sxs-lookup"><span data-stu-id="37e5e-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="37e5e-117">Este elemento se usa para generar archivos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="37e5e-117">This element is used to generate include files.</span></span> <span data-ttu-id="37e5e-118">Este elemento debe aparecer después de un elemento [**structDeclarations**](structdeclarations.md) para que las referencias entre estructuras se controlen correctamente.</span><span class="sxs-lookup"><span data-stu-id="37e5e-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="37e5e-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="37e5e-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="37e5e-120">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37e5e-120">Minimum supported system</span></span><br/> | <span data-ttu-id="37e5e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37e5e-121">Windows Vista</span></span> |
| <span data-ttu-id="37e5e-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="37e5e-122">Can be empty</span></span>                        | <span data-ttu-id="37e5e-123">Sí</span><span class="sxs-lookup"><span data-stu-id="37e5e-123">Yes</span></span>           |



 

 




