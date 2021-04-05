---
description: Define un servicio que se va a hospedar en una función de host Builder.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908661"
---
# <a name="hostedservice-element"></a><span data-ttu-id="9f109-103">hostedService (elemento)</span><span class="sxs-lookup"><span data-stu-id="9f109-103">hostedService element</span></span>

<span data-ttu-id="9f109-104">Define un servicio que se va a hospedar en una función de host Builder.</span><span class="sxs-lookup"><span data-stu-id="9f109-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="9f109-105">Uso</span><span class="sxs-lookup"><span data-stu-id="9f109-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="9f109-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f109-106">Attributes</span></span>

<span data-ttu-id="9f109-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="9f109-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9f109-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f109-108">Child elements</span></span>



| <span data-ttu-id="9f109-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f109-109">Element</span></span>                                     | <span data-ttu-id="9f109-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f109-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f109-111">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9f109-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="9f109-112">Especifica el nombre que se va a usar para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="9f109-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="9f109-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="9f109-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="9f109-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="9f109-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="9f109-115">Tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="9f109-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="9f109-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="9f109-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="9f109-117">Nombre de clase que se generará a partir de la función de generador.</span><span class="sxs-lookup"><span data-stu-id="9f109-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="9f109-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="9f109-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="9f109-119">URI que representa el identificador del servicio.</span><span class="sxs-lookup"><span data-stu-id="9f109-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="9f109-120">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f109-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="9f109-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9f109-121">Parent elements</span></span>



| <span data-ttu-id="9f109-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f109-122">Element</span></span>                         | <span data-ttu-id="9f109-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f109-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="9f109-124">**archivo**</span><span class="sxs-lookup"><span data-stu-id="9f109-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9f109-125">Especificación del archivo de salida para el generador de código.</span><span class="sxs-lookup"><span data-stu-id="9f109-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9f109-126">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9f109-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9f109-127">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f109-127">Minimum supported system</span></span><br/> | <span data-ttu-id="9f109-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f109-128">Windows Vista</span></span> |
| <span data-ttu-id="9f109-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9f109-129">Can be empty</span></span>                        | <span data-ttu-id="9f109-130">No</span><span class="sxs-lookup"><span data-stu-id="9f109-130">No</span></span>            |



 

 




