---
description: Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995322"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="9067b-103">elemento subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="9067b-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="9067b-104">Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="9067b-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9067b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="9067b-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="9067b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9067b-106">Attributes</span></span>



| <span data-ttu-id="9067b-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="9067b-107">Attribute</span></span>                 | <span data-ttu-id="9067b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9067b-108">Type</span></span>               | <span data-ttu-id="9067b-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9067b-109">Required</span></span>      | <span data-ttu-id="9067b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9067b-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9067b-111">**extensible**</span><span class="sxs-lookup"><span data-stu-id="9067b-111">**extensible**</span></span><br/> | <span data-ttu-id="9067b-112">boolean</span><span class="sxs-lookup"><span data-stu-id="9067b-112">boolean</span></span><br/> | <span data-ttu-id="9067b-113">No</span><span class="sxs-lookup"><span data-stu-id="9067b-113">No</span></span><br/> | <span data-ttu-id="9067b-114">La capacidad de agregar puntos de extensibilidad a funciones e interfaces.</span><span class="sxs-lookup"><span data-stu-id="9067b-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="9067b-115">Este valor siempre se establece en true.</span><span class="sxs-lookup"><span data-stu-id="9067b-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="9067b-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9067b-116">Child elements</span></span>



| <span data-ttu-id="9067b-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="9067b-117">Element</span></span>                                                           | <span data-ttu-id="9067b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9067b-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9067b-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="9067b-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="9067b-120">Especifica el nombre de la interfaz de notificación que se usa con las suscripciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="9067b-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="9067b-121">**Operación**</span><span class="sxs-lookup"><span data-stu-id="9067b-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="9067b-122">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="9067b-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="9067b-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="9067b-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="9067b-124">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="9067b-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="9067b-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="9067b-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="9067b-126">Especifica el nombre de la clase de proxy del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="9067b-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="9067b-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9067b-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9067b-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9067b-128">Parent elements</span></span>



| <span data-ttu-id="9067b-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="9067b-129">Element</span></span>                         | <span data-ttu-id="9067b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9067b-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9067b-131">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="9067b-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9067b-132">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="9067b-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9067b-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9067b-133">Element information</span></span>



| <span data-ttu-id="9067b-134">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9067b-134">Label</span></span> | <span data-ttu-id="9067b-135">Value</span><span class="sxs-lookup"><span data-stu-id="9067b-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9067b-136">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9067b-136">Minimum supported system</span></span><br/> | <span data-ttu-id="9067b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9067b-137">Windows Vista</span></span> |
| <span data-ttu-id="9067b-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9067b-138">Can be empty</span></span>                        | <span data-ttu-id="9067b-139">Sí</span><span class="sxs-lookup"><span data-stu-id="9067b-139">Yes</span></span>           |



 

 




