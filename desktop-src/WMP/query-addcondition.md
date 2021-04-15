---
title: Query. addCondition (método)
description: El método addCondition agrega una condición al objeto de consulta mediante la lógica y.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- método addCondition de Windows Media Player
- método addCondition de Windows Media Player, clase de consulta
- Clase de consulta de Windows Media Player, método addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708278"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="c113d-106">Query. addCondition (método)</span><span class="sxs-lookup"><span data-stu-id="c113d-106">Query.addCondition method</span></span>

<span data-ttu-id="c113d-107">El método **addCondition** agrega una condición al objeto de **consulta** mediante la lógica y.</span><span class="sxs-lookup"><span data-stu-id="c113d-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="c113d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c113d-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="c113d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c113d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c113d-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c113d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c113d-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="c113d-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="c113d-112">*operador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c113d-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c113d-113">**Cadena** que contiene el operador.</span><span class="sxs-lookup"><span data-stu-id="c113d-113">**String** containing the operator.</span></span> <span data-ttu-id="c113d-114">Vea la sección Comentarios para ver los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="c113d-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="c113d-115">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c113d-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c113d-116">**Cadena** que contiene el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="c113d-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c113d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c113d-117">Return value</span></span>

<span data-ttu-id="c113d-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c113d-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c113d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c113d-119">Remarks</span></span>

<span data-ttu-id="c113d-120">Las consultas compuestas que usan la **consulta** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c113d-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="c113d-121">Puede encontrar una lista de valores para el parámetro de *atributo* en la sección de [referencia de atributo alfabético](alphabetical-attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c113d-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="c113d-122">Las condiciones contenidas en un objeto de **consulta** se organizan en grupos de condiciones.</span><span class="sxs-lookup"><span data-stu-id="c113d-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="c113d-123">Varias condiciones dentro de un grupo de condiciones se concatenan siempre mediante la lógica y.</span><span class="sxs-lookup"><span data-stu-id="c113d-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="c113d-124">Los grupos de condiciones siempre se concatenan entre sí mediante la lógica o.</span><span class="sxs-lookup"><span data-stu-id="c113d-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="c113d-125">Para iniciar un nuevo grupo de condiciones, llame a **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="c113d-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="c113d-126">En la tabla siguiente se enumeran los valores admitidos para el *operador*.</span><span class="sxs-lookup"><span data-stu-id="c113d-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="c113d-127">Operator</span><span class="sxs-lookup"><span data-stu-id="c113d-127">Operator</span></span>            | <span data-ttu-id="c113d-128">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c113d-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="c113d-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="c113d-129">BeginsWith</span></span>          | <span data-ttu-id="c113d-130">Cadenas</span><span class="sxs-lookup"><span data-stu-id="c113d-130">Strings</span></span>        |
| <span data-ttu-id="c113d-131">Contiene</span><span class="sxs-lookup"><span data-stu-id="c113d-131">Contains</span></span>            | <span data-ttu-id="c113d-132">Cadenas</span><span class="sxs-lookup"><span data-stu-id="c113d-132">Strings</span></span>        |
| <span data-ttu-id="c113d-133">Equals</span><span class="sxs-lookup"><span data-stu-id="c113d-133">Equals</span></span>              | <span data-ttu-id="c113d-134">Todos los tipos</span><span class="sxs-lookup"><span data-stu-id="c113d-134">All types</span></span>      |
| <span data-ttu-id="c113d-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="c113d-135">GreaterThan</span></span>         | <span data-ttu-id="c113d-136">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="c113d-136">Numbers, Dates</span></span> |
| <span data-ttu-id="c113d-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="c113d-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="c113d-138">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="c113d-138">Numbers, Dates</span></span> |
| <span data-ttu-id="c113d-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="c113d-139">LessThan</span></span>            | <span data-ttu-id="c113d-140">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="c113d-140">Numbers, Dates</span></span> |
| <span data-ttu-id="c113d-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="c113d-141">LessThanOrEquals</span></span>    | <span data-ttu-id="c113d-142">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="c113d-142">Numbers, Dates</span></span> |
| <span data-ttu-id="c113d-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="c113d-143">NotBeginsWith</span></span>       | <span data-ttu-id="c113d-144">Cadenas</span><span class="sxs-lookup"><span data-stu-id="c113d-144">Strings</span></span>        |
| <span data-ttu-id="c113d-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="c113d-145">NotContains</span></span>         | <span data-ttu-id="c113d-146">Cadenas</span><span class="sxs-lookup"><span data-stu-id="c113d-146">Strings</span></span>        |
| <span data-ttu-id="c113d-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="c113d-147">NotEquals</span></span>           | <span data-ttu-id="c113d-148">Todos los tipos</span><span class="sxs-lookup"><span data-stu-id="c113d-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="c113d-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c113d-149">Examples</span></span>

<span data-ttu-id="c113d-150">En el siguiente ejemplo de JScript se usa **query. addCondition** y **query. beginNextGroup** para realizar una consulta de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c113d-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="c113d-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c113d-151">Requirements</span></span>



| <span data-ttu-id="c113d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c113d-152">Requirement</span></span> | <span data-ttu-id="c113d-153">Value</span><span class="sxs-lookup"><span data-stu-id="c113d-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c113d-154">Versión</span><span class="sxs-lookup"><span data-stu-id="c113d-154">Version</span></span><br/> | <span data-ttu-id="c113d-155">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c113d-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c113d-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c113d-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="c113d-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c113d-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c113d-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="c113d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c113d-159">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="c113d-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="c113d-160">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="c113d-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="c113d-161">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="c113d-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="c113d-162">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="c113d-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="c113d-163">**Consulta. beginNextGroup**</span><span class="sxs-lookup"><span data-stu-id="c113d-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





