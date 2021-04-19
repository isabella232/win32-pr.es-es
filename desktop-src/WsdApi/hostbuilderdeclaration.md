---
description: Genera una declaración para una función que crea un host con tipo.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706976"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="b560b-103">elemento hostBuilderDeclaration</span><span class="sxs-lookup"><span data-stu-id="b560b-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="b560b-104">Genera una declaración para una función que crea un host con tipo.</span><span class="sxs-lookup"><span data-stu-id="b560b-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="b560b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b560b-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="b560b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b560b-106">Attributes</span></span>

<span data-ttu-id="b560b-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b560b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b560b-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b560b-108">Child elements</span></span>



| <span data-ttu-id="b560b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b560b-109">Element</span></span>                                   | <span data-ttu-id="b560b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b560b-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b560b-111">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="b560b-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="b560b-112">Nombre de la interfaz de servicio que se va a incluir para el host.</span><span class="sxs-lookup"><span data-stu-id="b560b-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="b560b-113">El valor de este elemento debe coincidir con el valor del elemento secundario [**interface**](interface.md) de [**hostedService**](hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="b560b-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="b560b-114">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b560b-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="b560b-115">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b560b-115">Parent elements</span></span>



| <span data-ttu-id="b560b-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="b560b-116">Element</span></span>                         | <span data-ttu-id="b560b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b560b-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b560b-118">**archivo**</span><span class="sxs-lookup"><span data-stu-id="b560b-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b560b-119">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="b560b-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="b560b-120">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b560b-120">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b560b-121">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b560b-121">Minimum supported system</span></span><br/> | <span data-ttu-id="b560b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b560b-122">Windows Vista</span></span> |
| <span data-ttu-id="b560b-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b560b-123">Can be empty</span></span>                        | <span data-ttu-id="b560b-124">No</span><span class="sxs-lookup"><span data-stu-id="b560b-124">No</span></span>            |



 

 




