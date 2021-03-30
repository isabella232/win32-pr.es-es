---
title: Elemento Execution (SystemPropertiesType)
description: Contiene información sobre el proceso y el subproceso que registró el evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- EventLog del elemento de ejecución
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801418"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="6340b-104">Elemento Execution (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="6340b-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="6340b-105">Contiene información sobre el proceso y el subproceso que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="6340b-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6340b-106">El elemento de **ejecución** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6340b-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="6340b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6340b-107">Attributes</span></span>



| <span data-ttu-id="6340b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="6340b-108">Name</span></span>          | <span data-ttu-id="6340b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6340b-109">Type</span></span>         | <span data-ttu-id="6340b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6340b-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6340b-111">KernelTime</span><span class="sxs-lookup"><span data-stu-id="6340b-111">KernelTime</span></span>    | <span data-ttu-id="6340b-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-112">unsignedInt</span></span>  | <span data-ttu-id="6340b-113">Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="6340b-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="6340b-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="6340b-114">ProcessID</span></span>     | <span data-ttu-id="6340b-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-115">unsignedInt</span></span>  | <span data-ttu-id="6340b-116">Identifica el proceso que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="6340b-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="6340b-117">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="6340b-117">ProcessorID</span></span>   | <span data-ttu-id="6340b-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6340b-118">unsignedByte</span></span> | <span data-ttu-id="6340b-119">Número de identificación del procesador que procesó el evento.</span><span class="sxs-lookup"><span data-stu-id="6340b-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="6340b-120">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="6340b-120">ProcessorTime</span></span> | <span data-ttu-id="6340b-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-121">unsignedInt</span></span>  | <span data-ttu-id="6340b-122">En el caso de las sesiones privadas de ETW, el tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU.</span><span class="sxs-lookup"><span data-stu-id="6340b-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="6340b-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="6340b-123">SessionID</span></span>     | <span data-ttu-id="6340b-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-124">unsignedInt</span></span>  | <span data-ttu-id="6340b-125">Número de identificación de la sesión de Terminal Server en la que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="6340b-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="6340b-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="6340b-126">ThreadID</span></span>      | <span data-ttu-id="6340b-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-127">unsignedInt</span></span>  | <span data-ttu-id="6340b-128">Identifica el subproceso que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="6340b-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="6340b-129">UserTime</span><span class="sxs-lookup"><span data-stu-id="6340b-129">UserTime</span></span>      | <span data-ttu-id="6340b-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6340b-130">unsignedInt</span></span>  | <span data-ttu-id="6340b-131">Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="6340b-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="6340b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6340b-132">Requirements</span></span>



| <span data-ttu-id="6340b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6340b-133">Requirement</span></span> | <span data-ttu-id="6340b-134">Value</span><span class="sxs-lookup"><span data-stu-id="6340b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6340b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6340b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6340b-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6340b-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6340b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6340b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6340b-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6340b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6340b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6340b-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="6340b-140">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="6340b-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6340b-141">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="6340b-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="6340b-142">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="6340b-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6340b-143">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="6340b-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





