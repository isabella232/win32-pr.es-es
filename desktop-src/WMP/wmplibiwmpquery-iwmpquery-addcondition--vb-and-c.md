---
title: IWMPQuery addCondition, método
description: El método addCondition agrega una condición a la consulta compuesta mediante la lógica y.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- método addCondition de Windows Media Player
- método addCondition Windows Media Player, interfaz IWMPQuery
- Interfaz IWMPQuery Windows Media Player, método addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718882"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="d330a-106">IWMPQuery:: addCondition (método)</span><span class="sxs-lookup"><span data-stu-id="d330a-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="d330a-107">El método **addCondition** agrega una condición a la consulta compuesta mediante la lógica **y** .</span><span class="sxs-lookup"><span data-stu-id="d330a-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d330a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d330a-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="d330a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d330a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d330a-110">*bstrAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d330a-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d330a-111">**System. String** que es el nombre del atributo que se va a agregar a la consulta.</span><span class="sxs-lookup"><span data-stu-id="d330a-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="d330a-112">*bstrOperator* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d330a-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d330a-113">**System. String** que es el operador.</span><span class="sxs-lookup"><span data-stu-id="d330a-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="d330a-114">Vea la sección Comentarios para ver los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="d330a-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="d330a-115">*bstrValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d330a-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d330a-116">**System. String** que es el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="d330a-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d330a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d330a-117">Return value</span></span>

<span data-ttu-id="d330a-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d330a-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d330a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d330a-119">Remarks</span></span>

<span data-ttu-id="d330a-120">Las condiciones contenidas en una consulta compuesta se organizan en grupos de condiciones.</span><span class="sxs-lookup"><span data-stu-id="d330a-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="d330a-121">Varias condiciones dentro de un grupo de condiciones se concatenan siempre mediante la lógica **y** .</span><span class="sxs-lookup"><span data-stu-id="d330a-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="d330a-122">Los grupos de condiciones siempre se concatenan entre sí mediante la lógica **o** .</span><span class="sxs-lookup"><span data-stu-id="d330a-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="d330a-123">Para iniciar un nuevo grupo de condiciones, llame a [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="d330a-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="d330a-124">Las consultas compuestas que usan **IWMPQuery** no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d330a-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="d330a-125">Puede encontrar una lista de valores para el parámetro *bstrAttribute* en [referencia de atributo alfabético](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d330a-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="d330a-126">En la tabla siguiente se enumeran los valores admitidos para *bstrOperator*.</span><span class="sxs-lookup"><span data-stu-id="d330a-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="d330a-127">String</span><span class="sxs-lookup"><span data-stu-id="d330a-127">String</span></span>              | <span data-ttu-id="d330a-128">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d330a-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="d330a-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="d330a-129">BeginsWith</span></span>          | <span data-ttu-id="d330a-130">Cadenas</span><span class="sxs-lookup"><span data-stu-id="d330a-130">Strings</span></span>        |
| <span data-ttu-id="d330a-131">Contiene</span><span class="sxs-lookup"><span data-stu-id="d330a-131">Contains</span></span>            | <span data-ttu-id="d330a-132">Cadenas</span><span class="sxs-lookup"><span data-stu-id="d330a-132">Strings</span></span>        |
| <span data-ttu-id="d330a-133">Equals</span><span class="sxs-lookup"><span data-stu-id="d330a-133">Equals</span></span>              | <span data-ttu-id="d330a-134">Todos los tipos</span><span class="sxs-lookup"><span data-stu-id="d330a-134">All types</span></span>      |
| <span data-ttu-id="d330a-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="d330a-135">GreaterThan</span></span>         | <span data-ttu-id="d330a-136">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="d330a-136">Numbers, Dates</span></span> |
| <span data-ttu-id="d330a-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="d330a-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="d330a-138">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="d330a-138">Numbers, Dates</span></span> |
| <span data-ttu-id="d330a-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="d330a-139">LessThan</span></span>            | <span data-ttu-id="d330a-140">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="d330a-140">Numbers, Dates</span></span> |
| <span data-ttu-id="d330a-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="d330a-141">LessThanOrEquals</span></span>    | <span data-ttu-id="d330a-142">Números, fechas</span><span class="sxs-lookup"><span data-stu-id="d330a-142">Numbers, Dates</span></span> |
| <span data-ttu-id="d330a-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d330a-143">NotBeginsWith</span></span>       | <span data-ttu-id="d330a-144">Cadenas</span><span class="sxs-lookup"><span data-stu-id="d330a-144">Strings</span></span>        |
| <span data-ttu-id="d330a-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="d330a-145">NotContains</span></span>         | <span data-ttu-id="d330a-146">Cadenas</span><span class="sxs-lookup"><span data-stu-id="d330a-146">Strings</span></span>        |
| <span data-ttu-id="d330a-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="d330a-147">NotEquals</span></span>           | <span data-ttu-id="d330a-148">Todos los tipos</span><span class="sxs-lookup"><span data-stu-id="d330a-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="d330a-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d330a-149">Examples</span></span>

<span data-ttu-id="d330a-150">En el ejemplo siguiente se crea una consulta, se le agregan dos condiciones y se utiliza esa consulta para extraer los resultados de la consulta como una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="d330a-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="d330a-151">Los resultados se muestran en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d330a-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="d330a-152">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="d330a-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="d330a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d330a-153">Requirements</span></span>



| <span data-ttu-id="d330a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="d330a-154">Requirement</span></span> | <span data-ttu-id="d330a-155">Value</span><span class="sxs-lookup"><span data-stu-id="d330a-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d330a-156">Versión</span><span class="sxs-lookup"><span data-stu-id="d330a-156">Version</span></span><br/>   | <span data-ttu-id="d330a-157">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d330a-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="d330a-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d330a-158">Namespace</span></span><br/> | <span data-ttu-id="d330a-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d330a-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d330a-160">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d330a-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d330a-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d330a-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d330a-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="d330a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d330a-163">**Referencia de atributo alfabético**</span><span class="sxs-lookup"><span data-stu-id="d330a-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="d330a-164">**IWMPMediaCollection2. createQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d330a-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d330a-165">**IWMPMediaCollection2. getPlaylistByQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d330a-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d330a-166">**IWMPMediaCollection2. getStringCollectionByQuery (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d330a-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d330a-167">**Interfaz IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="d330a-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





