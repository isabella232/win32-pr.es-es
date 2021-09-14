---
description: Define un contador.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: counter Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a2af7ec5f9945257a94d1c65823ecad3c9a05f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069184"
---
# <a name="counter-complex-type"></a>counter Complex Type

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
| **counterAttributes** | [**man:counterAttributes**](performance-counters-counterattributes-complex-type.md) | Enumera los atributos únicos que especifican cómo se muestran los datos del contador en una aplicación de consumidor.<br/> |



## <a name="attributes"></a>Atributos




| Nombre | Tipo | Descripción | 
|------|------|-------------|
| aggregate | Función de agregación que se va a aplicar si el atributo <strong>instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> es globalAggregate, multipleAggregate o globalAggregateHistory. Estas son las posibles funciones de agregación que puede aplicar:<br /><dl><dt><span id="max"></span><span id="MAX"></span>max</dt><dd> Se devuelve el valor máximo del contador.<br /></dd><dt><span id="min"></span><span id="MIN"></span>Min</dt><dd> Se devuelve el valor mínimo del contador.<br /></dd><dt><span id="avg"></span><span id="AVG"></span>avg</dt><dd> Se devuelve el valor medio del contador.<br /></dd><dt><span id="sum"></span><span id="SUM"></span>Sum</dt><dd> Se devuelve la suma de los valores del contador.<br /></dd><dt><span id="undefined"></span><span id="UNDEFINED"></span>Indefinido</dt><dd> No agregue este contador.<br /></dd></dl> | 
| baseID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren un contador base:<br /><dl><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt><dd> Requiere el PERF_AVERAGE_BASE base.<br /></dd><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt><dd> Requiere el PERF_AVERAGE_BASE base.<br /></dd><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt><dd> Requiere el PERF_COUNTER_MULTI_BASE base.<br /></dd><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt><dd> Requiere el PERF_LARGE_RAW_BASE base.<br /></dd><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt><dd> Requiere el PERF_LARGE_RAW_BASE base.<br /></dd><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt><dd> Requiere el PERF_RAW_BASE base.<br /></dd><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt><dd> Requiere el PERF_SAMPLE_BASE base.<br /></dd></dl> | 
| defaultScale | Factor de escala que se aplicará al valor del contador (factor * valor del contador). El valor predeterminado es cero si no se aplica ninguna escala. Los valores válidos van de 10 a 10 (de 0,0000000001 a 100000000). Si este valor es cero, el valor de escala es 1; si este valor es 1, el valor de escala es 10; si este valor es 1, el valor de escala es .10; y así sucesivamente.<br /> | 
| description | <strong>xs:string</strong> | Breve descripción del contador. No es necesario especificar este atributo si el contador incluye el <a href="performance-counters-counterattribute-complex-type.md"><strong>atributo noDisplay.</strong></a><br /> | 
| detailLevel | Especifica la audiencia de destino para los detalles del contador. Los posibles valores son los siguientes:<br /><dl><dt><span id="standard"></span><span id="STANDARD"></span>Estándar</dt><dd> Mostrar detalles sobre el contador que un usuario típico entendería.<br /></dd><dt><span id="advanced"></span><span id="ADVANCED"></span>Avanzada</dt><dd> Mostrar detalles sobre el contador que solo un usuario avanzado entendería.<br /></dd></dl> | 
| campo | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | Nombre de un campo dentro de la estructura que contiene el valor del contador. Este atributo no se permite para los proveedores en modo de usuario.<br /> | 
| id | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Número único que identifica el contador dentro del conjunto de contadores.<br /> | 
| multiCounterID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor multiplicador se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren un valor multiplicador. El contador al que se hace referencia debe ser de tipo PERF_COUNTER_RAWCOUNT.<br /><ul><li>PERF_COUNTER_MULTI_TIMER</li><li>PERF_COUNTER_MULTI_TIMER_INV</li><li>PERF_100NSEC_MULTI_TIMER</li><li>PERF_100NSEC_MULTI_TIMER_INV</li></ul> | 
| name | Nombre del contador. El nombre debe ser único y tener menos de 1024 caracteres. El nombre distingue mayúsculas de minúsculas. No es necesario especificar este atributo si el contador incluye el <a href="performance-counters-counterattribute-complex-type.md"><strong>atributo noDisplay.</strong></a><br /> | 
| perfFreqID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de frecuencia se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren una frecuencia. El PERF_COUNTER_LARGE_RAWCOUNT tipo de contador contiene el valor de marca de tiempo.<br /><ul><li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li><li>PERF_ELAPSED_TIME</li><li>PERF_OBJ_TIME_TIMER</li><li>PERF_PRECISION_OBJECT_TIMER</li></ul> | 
| perfTimeID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Identificador de otro contador dentro del mismo conjunto de contadores, cuyo valor de marca de tiempo se usa para calcular el valor de este contador. Los siguientes tipos de contador requieren una marca de tiempo. El PERF_COUNTER_LARGE_RAWCOUNT tipo de contador contiene el valor de marca de tiempo.<br /><ul><li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li><li>PERF_ELAPSED_TIME</li><li>PERF_OBJ_TIME_TIMER</li><li>PERF_PRECISION_OBJECT_TIMER</li></ul> | 
| struct | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | Nombre de un elemento struct que contiene este valor de contador. Este atributo no se permite para los proveedores en modo de usuario.<br /> | 
| símbolo | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | Nombre simbólico que identifica el contador. La <a href="ctrpp.md">herramienta CTRPP</a> crea una constante que se puede usar al llamar a funciones que requieren un identificador de contador (por ejemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue).</strong></a> El nombre de la constante es el nombre simbólico.<br /> | 
| type | Nombre del tipo de contador. Para ver los valores posibles, consulte el bloque de sintaxis anterior. Para obtener más información sobre cada tipo, vea <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Tipos de contadores</a> en Windows Guía de implementación de 2003. El nombre distingue mayúsculas de minúsculas. <br /> | 
| uri | <strong>xs:anyURI</strong> | Identificador uniforme de recursos único que permite a los usuarios recuperar valores de contador de cualquier ubicación.<br /> | 




## <a name="remarks"></a>Observaciones

Para proporcionar compatibilidad con versiones anteriores, cada contador del conjunto de contadores debe especificar los mismos valores **perfFreqID** **y perfTimeID.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

