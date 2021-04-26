---
description: Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996412"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="b26b5-103">elemento stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="b26b5-103">stubDeclarations element</span></span>

<span data-ttu-id="b26b5-104">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b26b5-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b26b5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b26b5-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="b26b5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b26b5-106">Attributes</span></span>

<span data-ttu-id="b26b5-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b26b5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b26b5-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b26b5-108">Child elements</span></span>



| <span data-ttu-id="b26b5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b26b5-109">Element</span></span>                                   | <span data-ttu-id="b26b5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b26b5-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b26b5-111">**events**</span><span class="sxs-lookup"><span data-stu-id="b26b5-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="b26b5-112">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="b26b5-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="b26b5-113">**Operación**</span><span class="sxs-lookup"><span data-stu-id="b26b5-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b26b5-114">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="b26b5-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="b26b5-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="b26b5-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b26b5-116">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="b26b5-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="b26b5-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b26b5-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="b26b5-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b26b5-118">Parent elements</span></span>



| <span data-ttu-id="b26b5-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="b26b5-119">Element</span></span>                         | <span data-ttu-id="b26b5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b26b5-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b26b5-121">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b26b5-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b26b5-122">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="b26b5-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b26b5-123">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b26b5-123">Element information</span></span>



| <span data-ttu-id="b26b5-124">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b26b5-124">Label</span></span> | <span data-ttu-id="b26b5-125">Value</span><span class="sxs-lookup"><span data-stu-id="b26b5-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b26b5-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b26b5-126">Minimum supported system</span></span><br/> | <span data-ttu-id="b26b5-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b26b5-127">Windows Vista</span></span> |
| <span data-ttu-id="b26b5-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b26b5-128">Can be empty</span></span>                        | <span data-ttu-id="b26b5-129">Sí</span><span class="sxs-lookup"><span data-stu-id="b26b5-129">Yes</span></span>           |



 

 




