---
description: Especifica la información de tipo de una propiedad.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a70c6eeaee63bcb99ee19217ccff5d3ff7086a2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632173"
---
# <a name="typeinfo"></a>typeInfo

Especifica la información de tipo de una propiedad. Solo debe haber un [elemento typeInfo]() para cada [propertyDescription.](./propdesc-schema-propertydescription.md) Este elemento ha cambiado para Windows 7.

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [typeInfo,]() la configuración predeterminada del atributo se aplica a la descripción de la propiedad.

## <a name="syntax-for-windows-7"></a>Sintaxis para Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                   | Elementos secundarios |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>Público. Opcional. El valor predeterminado &quot; es Cualquier &quot; . Indica el tipo de la propiedad. Los siguientes son tipos válidos y <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>recupera sus tipos variantes asociados. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Any</td>
<td>Predeterminada. El subsistema de propiedades no aplicará ni forzará el valor de propiedad. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType devuelve</strong></a> VT_NULL. Se recomienda encarecidamente a los proveedores de software independientes (ISV) que proporcionen un tipo en lugar de volver a usar este valor predeterminado.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>No hay ningún valor para esta propiedad. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType devuelve</strong></a> VT_NULL.</td>
</tr>
<tr class="odd">
<td>String</td>
<td>El valor debe ser un VT_LPWSTR, que es una cadena Unicode terminada por una referencia nula.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>El valor debe ser un VT_BOOL, que es un valor booleano.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>El valor debe ser un VT_UI1, que es un byte.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>El valor debe ser un VT_UI1 | VT_VECTOR búfer de bytes.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>El valor debe ser VT_I2, que es un entero de 16 bits.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>El valor debe ser un VT_UI2, que es un entero de 16 bits sin signo.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>El valor debe ser VT_I4, que es un entero de 32 bits.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>El valor debe ser VT_UI4, que es un entero de 32 bits sin signo.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>El valor debe ser VT_I8, que es un entero de 64 bits.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>El valor debe ser un VT_UI8, que es un entero de 64 bits sin signo.</td>
</tr>
<tr class="odd">
<td>Doble</td>
<td>El valor debe ser un VT_R8, que es un valor double.</td>
</tr>
<tr class="even">
<td>DateTime</td>
<td>El valor debe ser VT_FILETIME, que es <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>filetime.</strong></a></td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>El valor debe ser un VT_CLSID, que es un identificador de clase (CLSID).</td>
</tr>
<tr class="even">
<td>Blob</td>
<td>El valor debe ser un VT_BLOB, que son bytes con prefijo de longitud.</td>
</tr>
<tr class="odd">
<td>STREAM</td>
<td>El valor debe ser VT_STREAM, que es un objeto que implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Portapapeles</td>
<td>El valor debe ser un VT_CF, que es un formato del Portapapeles.</td>
</tr>
<tr class="odd">
<td>Object</td>
<td>El valor debe ser VT_UNKNOWN, que es un objeto que implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>Opcional. El valor predeterminado &quot; es Discrete &quot; . Especifica cómo se muestra la propiedad cuando esta propiedad agrupa una vista. Una vez establecidos aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription::GetGroupingRange</strong></a>recupera estos valores. Los siguientes son tipos válidos.

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discrete</td>
<td>Predeterminada. Muestra valores individuales.</td>
</tr>
<tr class="even">
<td>Alfanuméricas</td>
<td>Muestra intervalos alfanuméricos estáticos para los valores.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Muestra intervalos de tamaño estáticos para los valores.</td>
</tr>
<tr class="even">
<td>Date</td>
<td>Muestra los grupos de mes y año. Valor predeterminado para las propiedades de tipo= &quot; &quot; DateTime.</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Se muestra en grupos relativos al tiempo.</td>
</tr>
<tr class="even">
<td>Dinámica</td>
<td>Muestra los intervalos creados dinámicamente para los valores.</td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Muestra depósitos de porcentaje.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si la propiedad se considera innate. Una propiedad innate es una propiedad que se calcula a partir del contenido de un archivo o de otros recursos o sistemas. Por ejemplo, System.Size es una propiedad innate proporcionada por el sistema de archivos; cambiar el valor de la propiedad en y de sí mismo no hace nada. Otros ejemplos son System.Image.Dimensions y System.Document. PageCount, que se calcula mediante programas basados en el contenido del archivo, no en función de una configuración modificable por el usuario. Establecer isInnate= &quot; true significa que el usuario no puede editar esta propiedad directamente a través de un control de &quot; propiedad. Este valor se asigna a la PDTF_ISINNATE definida <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>en PROPDESC_TYPE_FLAGS</strong></a> se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista con Service Pack 1 (SP1) y versiones posteriores solo</strong>. Público. Opcional. Cuando se establece &quot; en true , permite eliminar una propiedad &quot; innate. Las propiedades innate, que se calculan a partir de otras propiedades, son de solo lectura por definición. El valor predeterminado de este atributo depende del <em>valor isInnate.</em>

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>valor predeterminado canBePurged</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Una propiedad cuyo <em>valor isInnate</em> es false (lo que significa que la propiedad es de lectura y escritura) tampoco puede establecer el valor &quot; &quot; <em>canBePurged</em> en &quot; &quot; false. El sistema operativo aplica esta restricción.
</blockquote>
</div>
<div>
 
</div>
<p>Aunque este atributo se introdujo en Windows Vista con Service Pack 1 (SP1), un archivo .propdesc que incluye este atributo es compatible con Windows Vista antes de Windows Vista con SP1. El <em>atributo canBePurged</em> simplemente se omite en esa situación.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad puede tener varios valores. Este valor se asigna a la PDTF_MULTIPLEVALUES definida <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>en PROPDESC_TYPE_FLAGS</strong></a> y usada en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>. Esto también influye en si VT_VECTOR es OR'd al VARTYPE del valor de propiedad.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si la propiedad es un encabezado de grupo. Un encabezado de grupo se usa estrictamente en proplists, no tiene ningún valor, nunca se almacena en un archivo y también debe tener <typeInfo type=&quot;Null&quot;> . Alguna interfaz de usuario del sistema usa proplists para indicar la secuencia de las propiedades que se mostrarán. Estas listas de propiedades pueden incluir referencias a encabezados de grupo (por ejemplo, System.PropGroup.Camera), que le indicó a la interfaz de usuario que inicie una nueva sección de grupo (por ejemplo, &quot; Camera Configuración &quot; ). Una descripción de propiedad con isGroup= &quot; true debe especificar un ; de lo &quot; <labelInfo label=&quot;Some localized label&quot;> contrario, no es una propiedad útil. Este valor se asigna a la PDTF_ISGROUP definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>AggregationType</td>
<td>Público. Opcional. El valor predeterminado &quot; es Default &quot; . Especifica cómo se muestran las propiedades de agregado cuando se seleccionan varios elementos. Una vez establecidos aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> recupera estos valores como un <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Los siguientes son tipos válidos.

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predeterminado</td>
<td>Predeterminada. Muestra un marcador <strong>de posición Varios</strong> valores en la interfaz de usuario. Este es el valor predeterminado si <em>el tipo</em> no es compatible con el <em>elemento aggregationType especificado.</em></td>
</tr>
<tr class="even">
<td>Primero</td>
<td>Muestra el valor de propiedad del primer elemento de la selección o colección.</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Muestra la suma de los valores numéricos. Útil para propiedades como System.Media.Duration o System.Size. Este valor no es compatible con tipos no numéricos.</td>
</tr>
<tr class="even">
<td>Media</td>
<td>Muestra el promedio de los valores numéricos. Útil para propiedades como System.Rating. Este valor no es compatible con tipos no numéricos.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Muestra un intervalo de fechas. Útil para propiedades como System.Photo.DateTaken. Este valor no es compatible con nada excepto type= DateTime y es el &quot; valor predeterminado para las propiedades de ese &quot; tipo.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Muestra una unión de todos los valores de la selección o colección. El orden en el que se muestran los valores es indefinido. Este valor es el predeterminado para las propiedades de type= &quot; String &quot; y multipleValues= &quot; &quot; true.</td>
</tr>
<tr class="odd">
<td>Máxima</td>
<td>Muestra el valor máximo de la colección. Útil para propiedades como System.DateModified. No es compatible con tipos no numéricos o no de fecha.</td>
</tr>
<tr class="even">
<td>Mínima</td>
<td>Muestra el valor mínimo de la colección. No es compatible con tipos no numéricos o no de fecha.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>isTreeProperty</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isViewable</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad está pensada para ser visualizable para el usuario. Por ejemplo, la interfaz de usuario del elegidor de columnas solo muestra las propiedades que tienen isViewable= &quot; &quot; true. La excepción es la interfaz de usuario controlada por proplist, que siempre mostrará la propiedad . Si tiene una propiedad que solo está pensada para crear datos entre dos objetos y que nunca está pensada para que la vea el usuario, este atributo debe ser false. Este valor se asigna a la PDTF_ISVIEWABLE definida <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>en PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>Windows Solo Vista. No se admite en Windows 7 y versiones posteriores. Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad está pensada para estar disponible en la interfaz de usuario Generador de consultas búsqueda. Una propiedad debe tener isViewable= &quot; true antes de que se respete &quot; isQueryable= &quot; &quot; true. Este valor se asigna a la PDTF_ISQUERYABLE definida <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>en PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 y versiones posteriores.</strong> Público. Opcional. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Windows Solo Vista. No se admite en Windows 7 y versiones posteriores. Público. Opcional. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Público. Opcional. El valor predeterminado es &quot; &quot; String. Especifica una sugerencia a la interfaz de usuario de Generador de consultas búsqueda para que pueda determinar la lista de posibles operadores de condición dentro de un predicado. Los siguientes son valores reconocidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Predeterminada. Se usarán los operadores siguientes: es , no es , , , , , empieza por , termina con , contiene , no contiene &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; &quot; , es &quot; como &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Valor predeterminado para las propiedades numéricas. Se usarán los operadores siguientes: es igual a , no es igual a , es menor que , es mayor que , es menor o igual que , es mayor o &quot; &quot; igual que &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Valor predeterminado para las propiedades de tipo= &quot; &quot; DateTime. Se usarán los operadores siguientes: es , no es , es antes de , es después de , es anterior a pero incluye &quot; &quot; , es después de &quot; pero &quot; incluye &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Valor predeterminado para las propiedades de tipo= &quot; &quot; booleano. Igual que Número.</td>
</tr>
<tr class="odd">
<td>Size</td>
<td>Igual que Número.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Público. Opcional. El valor predeterminado &quot; es Igual &quot; a . Especifica una sugerencia a la herramienta de Generador de consultas búsqueda para que pueda determinar el operador predeterminado. Los valores posibles son los siguientes:

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Igual</td>
<td>Predeterminada. Indica equivalente.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Indica que no es equivalente.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Indica que es menor que.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Valor predeterminado para las propiedades de conditionType= &quot; Size &quot; . Indica mayor que.</td>
</tr>
<tr class="odd">
<td>Contiene</td>
<td>Valor predeterminado para las propiedades de conditionType= &quot; String &quot; . Indica la inclusión.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
