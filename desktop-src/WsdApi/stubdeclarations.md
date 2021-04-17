---
description: Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717291"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="523ed-103">elemento stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="523ed-103">stubDeclarations element</span></span>

<span data-ttu-id="523ed-104">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="523ed-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="523ed-105">Uso</span><span class="sxs-lookup"><span data-stu-id="523ed-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="523ed-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="523ed-106">Attributes</span></span>

<span data-ttu-id="523ed-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="523ed-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="523ed-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="523ed-108">Child elements</span></span>



| <span data-ttu-id="523ed-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="523ed-109">Element</span></span>                                   | <span data-ttu-id="523ed-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="523ed-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="523ed-111">**events**</span><span class="sxs-lookup"><span data-stu-id="523ed-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="523ed-112">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="523ed-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="523ed-113">**sesión**</span><span class="sxs-lookup"><span data-stu-id="523ed-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="523ed-114">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="523ed-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="523ed-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="523ed-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="523ed-116">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="523ed-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="523ed-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="523ed-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="523ed-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="523ed-118">Parent elements</span></span>



| <span data-ttu-id="523ed-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="523ed-119">Element</span></span>                         | <span data-ttu-id="523ed-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="523ed-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="523ed-121">**archivo**</span><span class="sxs-lookup"><span data-stu-id="523ed-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="523ed-122">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="523ed-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="523ed-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="523ed-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="523ed-124">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="523ed-124">Minimum supported system</span></span><br/> | <span data-ttu-id="523ed-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="523ed-125">Windows Vista</span></span> |
| <span data-ttu-id="523ed-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="523ed-126">Can be empty</span></span>                        | <span data-ttu-id="523ed-127">Sí</span><span class="sxs-lookup"><span data-stu-id="523ed-127">Yes</span></span>           |



 

 




