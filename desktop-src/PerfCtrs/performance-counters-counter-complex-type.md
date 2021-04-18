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
# <a name="counter-complex-type"></a>Counter (tipo complejo)

Define un contador.

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

## <a name="child-elements"></a>Elementos secundarios



| Elemento               | Tipo                                                                                 | Descripción                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **contraatributos** | [**Man: contraattributes**](performance-counters-counterattributes-complex-type.md) | Muestra los atributos únicos que especifican cómo se muestran los datos del contador en una aplicación de consumidor.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aggregate</td>

<td>Función de agregación que se va a aplicar si el atributo <strong>instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> es GlobalAggregate, multipleAggregate o globalAggregateHistory. A continuación se muestran las posibles funciones de agregación que se pueden aplicar:<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>máx.</dt> <dd> Se devuelve el valor de contador máximo.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>minuto</dt> <dd> Se devuelve el valor de contador mínimo.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>latencia</dt> <dd> Se devuelve el valor de contador promedio.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>Sume</dt> <dd> Se devuelve la suma de los valores del contador.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>indefinido</dt> <dd> No agregue este contador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td>El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor se utiliza para calcular el valor de este contador. Los siguientes tipos de contador requieren un contador base:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Requiere el contador base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Requiere el contador base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Requiere el contador base PERF_COUNTER_MULTI_BASE.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Requiere el contador base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Requiere el contador base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Requiere el contador base PERF_RAW_BASE.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Requiere el contador base PERF_SAMPLE_BASE.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>Factor de escala que se va a aplicar al valor de contador (factor * valor de contador). El valor predeterminado es cero si no se aplica ninguna escala. Los valores válidos van de 10 a 10 (de 0,0000000001 a 1 mil millones). Si este valor es cero, el valor de escala es 1; Si este valor es 1, el valor de escala es 10; Si este valor es 1, el valor de escala es. 10; etc.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Breve descripción del contador. No es necesario especificar este atributo si el contador incluye el atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Especifica la audiencia de destino para los detalles del contador. Los posibles valores son los siguientes:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>normal</dt> <dd> Muestra detalles sobre el contador que un usuario típico entendería.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>financieros</dt> <dd> Muestra detalles sobre el contador que solo un usuario avanzado entendería.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>campo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></td>
<td>Nombre de un campo dentro del struct que contiene el valor del contador. Este atributo no está permitido para los proveedores de modo de usuario.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td>Número único que identifica el contador en el conjunto de contadores.<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td>Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de multiplicador se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren un valor de multiplicador. El contador al que se hace referencia debe ser de tipo PERF_COUNTER_RAWCOUNT.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Nombre del contador. El nombre debe ser único y tener menos de 1.024 caracteres. El nombre distingue mayúsculas de minúsculas. No es necesario especificar este atributo si el contador incluye el atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td>El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de frecuencia se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren una frecuencia. El tipo de contador PERF_COUNTER_LARGE_RAWCOUNT contiene el valor de la marca de tiempo.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32Type</strong></a></td>
<td>El identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de marca de tiempo se utiliza para calcular el valor de este contador. Los siguientes tipos de contador requieren una marca de tiempo. El tipo de contador PERF_COUNTER_LARGE_RAWCOUNT contiene el valor de la marca de tiempo.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></td>
<td>Nombre de un elemento de estructura que contiene este valor de contador. Este atributo no está permitido para los proveedores de modo de usuario.<br/></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>Man: CSymbolType</strong></a></td>
<td>Nombre simbólico que identifica el contador. La herramienta <a href="ctrpp.md">CTRPP</a> crea una constante que se puede usar al llamar a funciones que requieren un identificador de contador (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>). El nombre de la constante es el nombre simbólico.<br/></td>
</tr>
<tr class="even">
<td>type</td>

<td>Nombre del tipo de contador. Para ver los valores posibles, vea el bloque de sintaxis anterior. Para obtener detalles de cada tipo, vea <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">tipos de contador</a> en la guía de implementación de Windows 2003. El nombre distingue mayúsculas de minúsculas. <br/></td>
</tr>
<tr class="odd">
<td>uri</td>
<td><strong>xs:anyURI</strong></td>
<td>Un identificador uniforme de recursos único que permite a los usuarios recuperar los valores de contador de cualquier ubicación.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Para proporcionar compatibilidad con versiones anteriores, cada contador del conjunto de contadores debe especificar los mismos valores de **perfFreqID** y **perfTimeID** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

