---
title: QueryType (tipo complejo)
description: Define un conjunto de consultas de selector y suprimidor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Registro de eventos de tipo complejo de QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150241"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="0dc44-104">QueryType (tipo complejo)</span><span class="sxs-lookup"><span data-stu-id="0dc44-104">QueryType Complex Type</span></span>

<span data-ttu-id="0dc44-105">Define un conjunto de consultas de selector y suprimidor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="0dc44-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0dc44-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0dc44-106">Child elements</span></span>



| <span data-ttu-id="0dc44-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0dc44-107">Element</span></span>                                                    | <span data-ttu-id="0dc44-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0dc44-108">Type</span></span> | <span data-ttu-id="0dc44-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc44-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dc44-110">**Seleccionar**</span><span class="sxs-lookup"><span data-stu-id="0dc44-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="0dc44-111">Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="0dc44-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="0dc44-112">Especifique el XPath en el cuerpo del texto de este elemento.</span><span class="sxs-lookup"><span data-stu-id="0dc44-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="0dc44-113">XPath está limitado a 32 expresiones.</span><span class="sxs-lookup"><span data-stu-id="0dc44-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="0dc44-114">**Suprimir**</span><span class="sxs-lookup"><span data-stu-id="0dc44-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="0dc44-115">Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="0dc44-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="0dc44-116">Especifique el XPath en el cuerpo del texto de este elemento.</span><span class="sxs-lookup"><span data-stu-id="0dc44-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="0dc44-117">XPath está limitado a 32 expresiones.</span><span class="sxs-lookup"><span data-stu-id="0dc44-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0dc44-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0dc44-118">Attributes</span></span>



| <span data-ttu-id="0dc44-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="0dc44-119">Name</span></span> | <span data-ttu-id="0dc44-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="0dc44-120">Type</span></span>   | <span data-ttu-id="0dc44-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc44-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc44-122">Identificador</span><span class="sxs-lookup"><span data-stu-id="0dc44-122">Id</span></span>   | <span data-ttu-id="0dc44-123">long</span><span class="sxs-lookup"><span data-stu-id="0dc44-123">long</span></span>   | <span data-ttu-id="0dc44-124">Identificador que identifica de forma única esta consulta en la lista de consultas.</span><span class="sxs-lookup"><span data-stu-id="0dc44-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="0dc44-125">El identificador es de base cero.</span><span class="sxs-lookup"><span data-stu-id="0dc44-125">The identifier is zero-based.</span></span> <span data-ttu-id="0dc44-126">Debe especificar un identificador si la lista de consultas contiene más de una consulta.</span><span class="sxs-lookup"><span data-stu-id="0dc44-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="0dc44-127">Ruta</span><span class="sxs-lookup"><span data-stu-id="0dc44-127">Path</span></span> | <span data-ttu-id="0dc44-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="0dc44-128">anyURI</span></span> | <span data-ttu-id="0dc44-129">El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="0dc44-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="0dc44-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="0dc44-130">Path</span></span> | <span data-ttu-id="0dc44-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="0dc44-131">anyURI</span></span> | <span data-ttu-id="0dc44-132">El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="0dc44-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="0dc44-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="0dc44-133">Path</span></span> | <span data-ttu-id="0dc44-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="0dc44-134">anyURI</span></span> | <span data-ttu-id="0dc44-135">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0dc44-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="0dc44-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dc44-136">Remarks</span></span>

<span data-ttu-id="0dc44-137">La consulta debe tener al menos una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="0dc44-137">The query must have at least one select statement.</span></span> <span data-ttu-id="0dc44-138">Para cada instrucción Suppress, debe haber al menos una instrucción SELECT que especifique la misma ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="0dc44-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="0dc44-139">Si la consulta SELECT y Suppress devuelve los mismos eventos, la instrucción Suppress tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="0dc44-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="0dc44-140">Si selecciona eventos de varios orígenes, los eventos se devuelven en el orden de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0dc44-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="0dc44-141">Si utiliza la marca de tiempo del sistema y la tasa de eventos es alta, es posible que más de un evento tenga la misma marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0dc44-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="0dc44-142">Cuando esto ocurre, el orden de los eventos se vuelve ambiguo y los eventos pueden aparecer desordenados.</span><span class="sxs-lookup"><span data-stu-id="0dc44-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="0dc44-143">Si especifica una ruta de acceso para una de las consultas de la lista de consultas, todas las consultas deben especificar una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="0dc44-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="0dc44-144">Si no especifica una ruta de acceso para todas las consultas, debe especificar la ruta de acceso al llamar a la función [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="0dc44-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc44-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc44-145">Requirements</span></span>



| <span data-ttu-id="0dc44-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc44-146">Requirement</span></span> | <span data-ttu-id="0dc44-147">Value</span><span class="sxs-lookup"><span data-stu-id="0dc44-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0dc44-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc44-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc44-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0dc44-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0dc44-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dc44-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc44-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dc44-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





