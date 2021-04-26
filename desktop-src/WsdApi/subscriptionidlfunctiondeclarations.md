---
description: Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d738dd06ccbf034702cbb7d6494a28a229d07
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995372"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="8c53a-103">elemento subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="8c53a-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="8c53a-104">Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8c53a-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="8c53a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8c53a-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="8c53a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c53a-106">Attributes</span></span>



| <span data-ttu-id="8c53a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="8c53a-107">Attribute</span></span>                 | <span data-ttu-id="8c53a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c53a-108">Type</span></span>               | <span data-ttu-id="8c53a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8c53a-109">Required</span></span>      | <span data-ttu-id="8c53a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c53a-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c53a-111">**extensible**</span><span class="sxs-lookup"><span data-stu-id="8c53a-111">**extensible**</span></span><br/> | <span data-ttu-id="8c53a-112">boolean</span><span class="sxs-lookup"><span data-stu-id="8c53a-112">boolean</span></span><br/> | <span data-ttu-id="8c53a-113">No</span><span class="sxs-lookup"><span data-stu-id="8c53a-113">No</span></span><br/> | <span data-ttu-id="8c53a-114">La capacidad de agregar puntos de extensibilidad a funciones e interfaces.</span><span class="sxs-lookup"><span data-stu-id="8c53a-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="8c53a-115">Este valor siempre se establece en true.</span><span class="sxs-lookup"><span data-stu-id="8c53a-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="8c53a-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c53a-116">Child elements</span></span>



| <span data-ttu-id="8c53a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c53a-117">Element</span></span>                                                           | <span data-ttu-id="8c53a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c53a-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c53a-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="8c53a-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="8c53a-120">Especifica el nombre de la interfaz de notificación que se usa con las suscripciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="8c53a-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="8c53a-121">**Operación**</span><span class="sxs-lookup"><span data-stu-id="8c53a-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="8c53a-122">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="8c53a-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="8c53a-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="8c53a-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="8c53a-124">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="8c53a-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="8c53a-125">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c53a-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8c53a-126">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8c53a-126">Parent elements</span></span>



| <span data-ttu-id="8c53a-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c53a-127">Element</span></span>                         | <span data-ttu-id="8c53a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c53a-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8c53a-129">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8c53a-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8c53a-130">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="8c53a-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="8c53a-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8c53a-131">Element information</span></span>



| <span data-ttu-id="8c53a-132">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8c53a-132">Label</span></span> | <span data-ttu-id="8c53a-133">Value</span><span class="sxs-lookup"><span data-stu-id="8c53a-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8c53a-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c53a-134">Minimum supported system</span></span><br/> | <span data-ttu-id="8c53a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c53a-135">Windows Vista</span></span> |
| <span data-ttu-id="8c53a-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8c53a-136">Can be empty</span></span>                        | <span data-ttu-id="8c53a-137">Sí</span><span class="sxs-lookup"><span data-stu-id="8c53a-137">Yes</span></span>           |



 

 




