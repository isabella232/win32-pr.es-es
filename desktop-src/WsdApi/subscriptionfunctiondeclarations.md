---
description: Genera declaraciones de implementación para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279617"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="1c9cf-103">elemento subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="1c9cf-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="1c9cf-104">Genera declaraciones de implementación para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="1c9cf-105">Uso</span><span class="sxs-lookup"><span data-stu-id="1c9cf-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="1c9cf-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c9cf-106">Attributes</span></span>



| <span data-ttu-id="1c9cf-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="1c9cf-107">Attribute</span></span>                 | <span data-ttu-id="1c9cf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c9cf-108">Type</span></span>               | <span data-ttu-id="1c9cf-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1c9cf-109">Required</span></span>      | <span data-ttu-id="1c9cf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c9cf-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9cf-111">**extensible**</span><span class="sxs-lookup"><span data-stu-id="1c9cf-111">**extensible**</span></span><br/> | <span data-ttu-id="1c9cf-112">boolean</span><span class="sxs-lookup"><span data-stu-id="1c9cf-112">boolean</span></span><br/> | <span data-ttu-id="1c9cf-113">No</span><span class="sxs-lookup"><span data-stu-id="1c9cf-113">No</span></span><br/> | <span data-ttu-id="1c9cf-114">La capacidad de agregar puntos de extensibilidad a funciones e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="1c9cf-115">Este valor siempre se establece en true.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="1c9cf-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c9cf-116">Child elements</span></span>



| <span data-ttu-id="1c9cf-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c9cf-117">Element</span></span>                                                           | <span data-ttu-id="1c9cf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c9cf-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c9cf-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="1c9cf-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="1c9cf-120">Especifica el nombre de la interfaz de notificación utilizada con las suscripciones de evento.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="1c9cf-121">**sesión**</span><span class="sxs-lookup"><span data-stu-id="1c9cf-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="1c9cf-122">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="1c9cf-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="1c9cf-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="1c9cf-124">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="1c9cf-125">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c9cf-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1c9cf-126">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1c9cf-126">Parent elements</span></span>



| <span data-ttu-id="1c9cf-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c9cf-127">Element</span></span>                         | <span data-ttu-id="1c9cf-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c9cf-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1c9cf-129">**archivo**</span><span class="sxs-lookup"><span data-stu-id="1c9cf-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1c9cf-130">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="1c9cf-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1c9cf-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1c9cf-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1c9cf-132">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c9cf-132">Minimum supported system</span></span><br/> | <span data-ttu-id="1c9cf-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c9cf-133">Windows Vista</span></span> |
| <span data-ttu-id="1c9cf-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1c9cf-134">Can be empty</span></span>                        | <span data-ttu-id="1c9cf-135">Sí</span><span class="sxs-lookup"><span data-stu-id="1c9cf-135">Yes</span></span>           |



 

 




