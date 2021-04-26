---
description: Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995462"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="9092f-103">elemento subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="9092f-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="9092f-104">Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="9092f-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9092f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="9092f-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="9092f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9092f-106">Attributes</span></span>



| <span data-ttu-id="9092f-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="9092f-107">Attribute</span></span>                 | <span data-ttu-id="9092f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9092f-108">Type</span></span>               | <span data-ttu-id="9092f-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9092f-109">Required</span></span>      | <span data-ttu-id="9092f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9092f-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9092f-111">**extensible**</span><span class="sxs-lookup"><span data-stu-id="9092f-111">**extensible**</span></span><br/> | <span data-ttu-id="9092f-112">boolean</span><span class="sxs-lookup"><span data-stu-id="9092f-112">boolean</span></span><br/> | <span data-ttu-id="9092f-113">No</span><span class="sxs-lookup"><span data-stu-id="9092f-113">No</span></span><br/> | <span data-ttu-id="9092f-114">La capacidad de agregar puntos de extensibilidad a funciones e interfaces.</span><span class="sxs-lookup"><span data-stu-id="9092f-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="9092f-115">Este valor siempre se establece en true.</span><span class="sxs-lookup"><span data-stu-id="9092f-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="9092f-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9092f-116">Child elements</span></span>



| <span data-ttu-id="9092f-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="9092f-117">Element</span></span>                                                           | <span data-ttu-id="9092f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9092f-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9092f-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="9092f-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="9092f-120">Especifica el nombre de la interfaz de notificación que se usa con las suscripciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="9092f-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="9092f-121">**Operación**</span><span class="sxs-lookup"><span data-stu-id="9092f-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="9092f-122">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="9092f-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="9092f-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="9092f-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="9092f-124">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="9092f-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="9092f-125">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9092f-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9092f-126">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="9092f-126">Parent elements</span></span>



| <span data-ttu-id="9092f-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="9092f-127">Element</span></span>                         | <span data-ttu-id="9092f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9092f-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9092f-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="9092f-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9092f-130">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="9092f-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9092f-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9092f-131">Element information</span></span>



| <span data-ttu-id="9092f-132">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9092f-132">Label</span></span> | <span data-ttu-id="9092f-133">Value</span><span class="sxs-lookup"><span data-stu-id="9092f-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9092f-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9092f-134">Minimum supported system</span></span><br/> | <span data-ttu-id="9092f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9092f-135">Windows Vista</span></span> |
| <span data-ttu-id="9092f-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9092f-136">Can be empty</span></span>                        | <span data-ttu-id="9092f-137">Sí</span><span class="sxs-lookup"><span data-stu-id="9092f-137">Yes</span></span>           |



 

 




