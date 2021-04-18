---
description: Define un contador.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Counter (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667298"
---
# <a name="counter-complex-type"></a><span data-ttu-id="fb88c-103">Counter (tipo complejo)</span><span class="sxs-lookup"><span data-stu-id="fb88c-103">counter Complex Type</span></span>

<span data-ttu-id="fb88c-104">Define un contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-104">Defines a counter.</span></span>

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fb88c-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb88c-105">Child elements</span></span>



| <span data-ttu-id="fb88c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fb88c-106">Element</span></span>               | <span data-ttu-id="fb88c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb88c-107">Type</span></span>                                                                                 | <span data-ttu-id="fb88c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb88c-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb88c-109">**contraatributos**</span><span class="sxs-lookup"><span data-stu-id="fb88c-109">**counterAttributes**</span></span> | [<span data-ttu-id="fb88c-110">**Man: contraattributes**</span><span class="sxs-lookup"><span data-stu-id="fb88c-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="fb88c-111">Muestra los atributos únicos que especifican cómo se muestran los datos del contador en una aplicación de consumidor.</span><span class="sxs-lookup"><span data-stu-id="fb88c-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="fb88c-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb88c-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb88c-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb88c-113">Name</span></span></th>
<th><span data-ttu-id="fb88c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb88c-114">Type</span></span></th>
<th><span data-ttu-id="fb88c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb88c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb88c-116">aggregate</span><span class="sxs-lookup"><span data-stu-id="fb88c-116">aggregate</span></span></td>

<td><span data-ttu-id="fb88c-117">Función de agregación que se va a aplicar si el atributo <strong>instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> es GlobalAggregate, multipleAggregate o globalAggregateHistory.</span><span class="sxs-lookup"><span data-stu-id="fb88c-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="fb88c-118">A continuación se muestran las posibles funciones de agregación que se pueden aplicar:</span><span class="sxs-lookup"><span data-stu-id="fb88c-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="fb88c-119"><dt><span id="max"></span><span id="MAX"></span>máx.</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="fb88c-120">Se devuelve el valor de contador máximo.</span><span class="sxs-lookup"><span data-stu-id="fb88c-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="fb88c-121"><dt><span id="min"></span><span id="MIN"></span>minuto</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="fb88c-122">Se devuelve el valor de contador mínimo.</span><span class="sxs-lookup"><span data-stu-id="fb88c-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="fb88c-123"><dt><span id="avg"></span><span id="AVG"></span>latencia</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="fb88c-124">Se devuelve el valor de contador promedio.</span><span class="sxs-lookup"><span data-stu-id="fb88c-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="fb88c-125"><dt><span id="sum"></span><span id="SUM"></span>Sume</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="fb88c-126">Se devuelve la suma de los valores del contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="fb88c-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>indefinido</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="fb88c-128">No agregue este contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-129">baseID</span><span class="sxs-lookup"><span data-stu-id="fb88c-129">baseID</span></span></td>
<td><span data-ttu-id="fb88c-130"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-131">El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor se utiliza para calcular el valor de este contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="fb88c-132">Los siguientes tipos de contador requieren un contador base:</span><span class="sxs-lookup"><span data-stu-id="fb88c-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="fb88c-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="fb88c-134">Requiere el contador base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="fb88c-136">Requiere el contador base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="fb88c-138">Requiere el contador base PERF_COUNTER_MULTI_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="fb88c-140">Requiere el contador base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="fb88c-142">Requiere el contador base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="fb88c-144">Requiere el contador base PERF_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="fb88c-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="fb88c-146">Requiere el contador base PERF_SAMPLE_BASE.</span><span class="sxs-lookup"><span data-stu-id="fb88c-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-147">defaultScale</span><span class="sxs-lookup"><span data-stu-id="fb88c-147">defaultScale</span></span></td>

<td><span data-ttu-id="fb88c-148">Factor de escala que se va a aplicar al valor de contador (factor \* valor de contador).</span><span class="sxs-lookup"><span data-stu-id="fb88c-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="fb88c-149">El valor predeterminado es cero si no se aplica ninguna escala.</span><span class="sxs-lookup"><span data-stu-id="fb88c-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="fb88c-150">Los valores válidos van de 10 a 10 (de 0,0000000001 a 1 mil millones).</span><span class="sxs-lookup"><span data-stu-id="fb88c-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="fb88c-151">Si este valor es cero, el valor de escala es 1; Si este valor es 1, el valor de escala es 10; Si este valor es 1, el valor de escala es. 10; etc.</span><span class="sxs-lookup"><span data-stu-id="fb88c-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-152">description</span><span class="sxs-lookup"><span data-stu-id="fb88c-152">description</span></span></td>
<td><span data-ttu-id="fb88c-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="fb88c-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="fb88c-154">Breve descripción del contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-154">A short description of the counter.</span></span> <span data-ttu-id="fb88c-155">No es necesario especificar este atributo si el contador incluye el atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb88c-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="fb88c-156">detailLevel</span></span></td>

<td><span data-ttu-id="fb88c-157">Especifica la audiencia de destino para los detalles del contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="fb88c-158">Los posibles valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fb88c-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="fb88c-159"><dt><span id="standard"></span><span id="STANDARD"></span>normal</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="fb88c-160">Muestra detalles sobre el contador que un usuario típico entendería.</span><span class="sxs-lookup"><span data-stu-id="fb88c-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="fb88c-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>financieros</dt> </span><span class="sxs-lookup"><span data-stu-id="fb88c-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="fb88c-162">Muestra detalles sobre el contador que solo un usuario avanzado entendería.</span><span class="sxs-lookup"><span data-stu-id="fb88c-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-163">campo</span><span class="sxs-lookup"><span data-stu-id="fb88c-163">field</span></span></td>
<td><span data-ttu-id="fb88c-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-165">Nombre de un campo dentro del struct que contiene el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="fb88c-166">Este atributo no está permitido para los proveedores de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="fb88c-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-167">id</span><span class="sxs-lookup"><span data-stu-id="fb88c-167">id</span></span></td>
<td><span data-ttu-id="fb88c-168"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-169">Número único que identifica el contador en el conjunto de contadores.</span><span class="sxs-lookup"><span data-stu-id="fb88c-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-170">multiCounterID</span><span class="sxs-lookup"><span data-stu-id="fb88c-170">multiCounterID</span></span></td>
<td><span data-ttu-id="fb88c-171"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-172">Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de multiplicador se usa para calcular el valor de este contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="fb88c-173">Los siguientes tipos de contador requieren un valor de multiplicador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="fb88c-174">El contador al que se hace referencia debe ser de tipo PERF_COUNTER_RAWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="fb88c-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="fb88c-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="fb88c-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="fb88c-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="fb88c-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="fb88c-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="fb88c-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-179">name</span><span class="sxs-lookup"><span data-stu-id="fb88c-179">name</span></span></td>

<td><span data-ttu-id="fb88c-180">Nombre del contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-180">The name of the counter.</span></span> <span data-ttu-id="fb88c-181">El nombre debe ser único y tener menos de 1.024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fb88c-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="fb88c-182">El nombre distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb88c-182">The name is case-sensitive.</span></span> <span data-ttu-id="fb88c-183">No es necesario especificar este atributo si el contador incluye el atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fb88c-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-184">perfFreqID</span><span class="sxs-lookup"><span data-stu-id="fb88c-184">perfFreqID</span></span></td>
<td><span data-ttu-id="fb88c-185"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-186">El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de frecuencia se usa para calcular el valor de este contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="fb88c-187">Los siguientes tipos de contador requieren una frecuencia.</span><span class="sxs-lookup"><span data-stu-id="fb88c-187">The following counter types require a frequency.</span></span> <span data-ttu-id="fb88c-188">El tipo de contador PERF_COUNTER_LARGE_RAWCOUNT contiene el valor de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb88c-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="fb88c-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="fb88c-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="fb88c-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="fb88c-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="fb88c-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="fb88c-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-193">perfTimeID</span><span class="sxs-lookup"><span data-stu-id="fb88c-193">perfTimeID</span></span></td>
<td><span data-ttu-id="fb88c-194"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-195">El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de marca de tiempo se utiliza para calcular el valor de este contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="fb88c-196">Los siguientes tipos de contador requieren una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb88c-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="fb88c-197">El tipo de contador PERF_COUNTER_LARGE_RAWCOUNT contiene el valor de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb88c-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="fb88c-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="fb88c-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="fb88c-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="fb88c-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="fb88c-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="fb88c-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="fb88c-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-202">struct</span><span class="sxs-lookup"><span data-stu-id="fb88c-202">struct</span></span></td>
<td><span data-ttu-id="fb88c-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-204">Nombre de un elemento de estructura que contiene este valor de contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="fb88c-205">Este atributo no está permitido para los proveedores de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="fb88c-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-206">símbolo</span><span class="sxs-lookup"><span data-stu-id="fb88c-206">symbol</span></span></td>
<td><span data-ttu-id="fb88c-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="fb88c-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="fb88c-208">Nombre simbólico que identifica el contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="fb88c-209">La herramienta <a href="ctrpp.md">CTRPP</a> crea una constante que se puede usar al llamar a funciones que requieren un identificador de contador (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="fb88c-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="fb88c-210">El nombre de la constante es el nombre simbólico.</span><span class="sxs-lookup"><span data-stu-id="fb88c-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb88c-211">type</span><span class="sxs-lookup"><span data-stu-id="fb88c-211">type</span></span></td>

<td><span data-ttu-id="fb88c-212">Nombre del tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="fb88c-212">The name of the counter type.</span></span> <span data-ttu-id="fb88c-213">Para ver los valores posibles, vea el bloque de sintaxis anterior.</span><span class="sxs-lookup"><span data-stu-id="fb88c-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="fb88c-214">Para obtener detalles de cada tipo, vea <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">tipos de contador</a> en la guía de implementación de Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="fb88c-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="fb88c-215">El nombre distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb88c-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb88c-216">uri</span><span class="sxs-lookup"><span data-stu-id="fb88c-216">uri</span></span></td>
<td><span data-ttu-id="fb88c-217"><strong>xs:anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="fb88c-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="fb88c-218">Un identificador uniforme de recursos único que permite a los usuarios recuperar los valores de contador de cualquier ubicación.</span><span class="sxs-lookup"><span data-stu-id="fb88c-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="fb88c-219">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb88c-219">Remarks</span></span>

<span data-ttu-id="fb88c-220">Para proporcionar compatibilidad con versiones anteriores, cada contador del conjunto de contadores debe especificar los mismos valores de **perfFreqID** y **perfTimeID** .</span><span class="sxs-lookup"><span data-stu-id="fb88c-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb88c-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb88c-221">Requirements</span></span>



| <span data-ttu-id="fb88c-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb88c-222">Requirement</span></span> | <span data-ttu-id="fb88c-223">Value</span><span class="sxs-lookup"><span data-stu-id="fb88c-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb88c-224">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb88c-224">Minimum supported client</span></span><br/> | <span data-ttu-id="fb88c-225">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb88c-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb88c-226">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb88c-226">Minimum supported server</span></span><br/> | <span data-ttu-id="fb88c-227">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb88c-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

