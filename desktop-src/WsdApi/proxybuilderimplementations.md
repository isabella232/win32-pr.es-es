---
description: Genera funciones para crear servidores proxy con tipo.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706839"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="7cba5-103">elemento proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="7cba5-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="7cba5-104">Genera funciones para crear servidores proxy con tipo.</span><span class="sxs-lookup"><span data-stu-id="7cba5-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="7cba5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7cba5-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="7cba5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cba5-106">Attributes</span></span>

<span data-ttu-id="7cba5-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7cba5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7cba5-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cba5-108">Child elements</span></span>



| <span data-ttu-id="7cba5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7cba5-109">Element</span></span>                                     | <span data-ttu-id="7cba5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cba5-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cba5-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7cba5-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="7cba5-112">Nombre que se va a usar para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="7cba5-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="7cba5-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7cba5-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="7cba5-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="7cba5-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="7cba5-115">Tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="7cba5-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="7cba5-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="7cba5-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="7cba5-117">Nombre de clase que se generará a partir de la función de generador de proxy.</span><span class="sxs-lookup"><span data-stu-id="7cba5-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="7cba5-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cba5-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="7cba5-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7cba5-119">Parent elements</span></span>



| <span data-ttu-id="7cba5-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="7cba5-120">Element</span></span>                         | <span data-ttu-id="7cba5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cba5-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7cba5-122">**archivo**</span><span class="sxs-lookup"><span data-stu-id="7cba5-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7cba5-123">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="7cba5-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="7cba5-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7cba5-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7cba5-125">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cba5-125">Minimum supported system</span></span><br/> | <span data-ttu-id="7cba5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cba5-126">Windows Vista</span></span> |
| <span data-ttu-id="7cba5-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7cba5-127">Can be empty</span></span>                        | <span data-ttu-id="7cba5-128">No</span><span class="sxs-lookup"><span data-stu-id="7cba5-128">No</span></span>            |



 

 




