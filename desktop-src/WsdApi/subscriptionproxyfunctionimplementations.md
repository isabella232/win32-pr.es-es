---
description: Genera implementaciones para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154237"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="fcbff-103">elemento subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="fcbff-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="fcbff-104">Genera implementaciones para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="fcbff-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="fcbff-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fcbff-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="fcbff-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fcbff-106">Attributes</span></span>



| <span data-ttu-id="fcbff-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="fcbff-107">Attribute</span></span>                 | <span data-ttu-id="fcbff-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fcbff-108">Type</span></span>               | <span data-ttu-id="fcbff-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fcbff-109">Required</span></span>      | <span data-ttu-id="fcbff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcbff-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbff-111">**extensible**</span><span class="sxs-lookup"><span data-stu-id="fcbff-111">**extensible**</span></span><br/> | <span data-ttu-id="fcbff-112">boolean</span><span class="sxs-lookup"><span data-stu-id="fcbff-112">boolean</span></span><br/> | <span data-ttu-id="fcbff-113">No</span><span class="sxs-lookup"><span data-stu-id="fcbff-113">No</span></span><br/> | <span data-ttu-id="fcbff-114">La capacidad de agregar puntos de extensibilidad a funciones e interfaces.</span><span class="sxs-lookup"><span data-stu-id="fcbff-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="fcbff-115">Este valor siempre se establece en true.</span><span class="sxs-lookup"><span data-stu-id="fcbff-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="fcbff-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fcbff-116">Child elements</span></span>



| <span data-ttu-id="fcbff-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="fcbff-117">Element</span></span>                                                           | <span data-ttu-id="fcbff-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcbff-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcbff-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="fcbff-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="fcbff-120">Especifica el nombre de la interfaz de notificación utilizada con las suscripciones de evento.</span><span class="sxs-lookup"><span data-stu-id="fcbff-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="fcbff-121">**sesión**</span><span class="sxs-lookup"><span data-stu-id="fcbff-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="fcbff-122">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="fcbff-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="fcbff-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="fcbff-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="fcbff-124">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="fcbff-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="fcbff-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="fcbff-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="fcbff-126">Especifica el nombre de la clase de proxy del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="fcbff-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="fcbff-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fcbff-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="fcbff-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fcbff-128">Parent elements</span></span>



| <span data-ttu-id="fcbff-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="fcbff-129">Element</span></span>                         | <span data-ttu-id="fcbff-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcbff-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fcbff-131">**archivo**</span><span class="sxs-lookup"><span data-stu-id="fcbff-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fcbff-132">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="fcbff-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fcbff-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fcbff-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fcbff-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcbff-134">Minimum supported system</span></span><br/> | <span data-ttu-id="fcbff-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcbff-135">Windows Vista</span></span> |
| <span data-ttu-id="fcbff-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fcbff-136">Can be empty</span></span>                        | <span data-ttu-id="fcbff-137">Sí</span><span class="sxs-lookup"><span data-stu-id="fcbff-137">Yes</span></span>           |



 

 




