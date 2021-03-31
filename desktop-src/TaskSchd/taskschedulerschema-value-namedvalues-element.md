---
title: Elemento Value (namedValues)
description: Contiene el valor que está asociado a un nombre en un par nombre-valor.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Elemento Value Programador de tareas
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803638"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="f9b22-104">Elemento Value (namedValues)</span><span class="sxs-lookup"><span data-stu-id="f9b22-104">Value (namedValues) Element</span></span>

<span data-ttu-id="f9b22-105">Contiene el valor que está asociado a un nombre en un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="f9b22-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="f9b22-106">El elemento de **valor** se define mediante el tipo complejo de [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b22-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9b22-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f9b22-107">Parent element</span></span>



| <span data-ttu-id="f9b22-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9b22-108">Element</span></span>                                                                                              | <span data-ttu-id="f9b22-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f9b22-109">Derived from</span></span>                                                       | <span data-ttu-id="f9b22-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9b22-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9b22-111">**ValueQueries (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="f9b22-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="f9b22-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="f9b22-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="f9b22-113">Especifica una colección de consultas XPath con nombre.</span><span class="sxs-lookup"><span data-stu-id="f9b22-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="f9b22-114">Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en el elemento [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b22-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="f9b22-115">El nombre de la consulta se puede usar como una variable en el mensaje de una acción ShowMessage.</span><span class="sxs-lookup"><span data-stu-id="f9b22-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9b22-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9b22-116">Remarks</span></span>

<span data-ttu-id="f9b22-117">Para el desarrollo de C++, vea la [**propiedad Value de ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="f9b22-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="f9b22-118">Para el desarrollo de scripts, vea [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="f9b22-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b22-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b22-119">Requirements</span></span>



| <span data-ttu-id="f9b22-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b22-120">Requirement</span></span> | <span data-ttu-id="f9b22-121">Value</span><span class="sxs-lookup"><span data-stu-id="f9b22-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9b22-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b22-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9b22-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9b22-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9b22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b22-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9b22-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





