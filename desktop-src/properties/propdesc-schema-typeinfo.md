---
description: Especifica la información de tipo de una propiedad.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: Requerida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666850"
---
# <a name="typeinfo"></a>Requerida

Especifica la información de tipo de una propiedad. Solo debe haber un elemento [typeInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md). Este elemento ha cambiado para Windows 7.

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [typeInfo]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.

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
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Público. Opcional. El valor predeterminado es &quot; any &quot; . Indica el tipo de la propiedad. Los siguientes son tipos válidos y sus tipos de variante asociados se recuperan mediante <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a>. 
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
<td>Predeterminada. El subsistema de propiedades no aplicará ni convertirá el valor de propiedad. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> devuelve VT_NULL. Se recomienda encarecidamente a los fabricantes de software independientes (ISV) que proporcionen un tipo en lugar de revertir a este valor predeterminado.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>No hay ningún valor para esta propiedad. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> devuelve VT_NULL.</td>
</tr>
<tr class="odd">
<td>String</td>
<td>El valor debe ser un VT_LPWSTR, que es una cadena Unicode que termina en una referencia nula.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>El valor debe ser un VT_BOOL, que es un booleano.</td>
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
<td>El valor debe ser un VT_I2, que es un entero de 16 bits.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>El valor debe ser un VT_UI2, que es un entero sin signo de 16 bits.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>El valor debe ser un VT_I4, que es un entero de 32 bits.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>El valor debe ser un VT_UI4, que es un entero de 32 bits sin signo.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>El valor debe ser un VT_I8, que es un entero de 64 bits.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>El valor debe ser un VT_UI8, que es un entero de 64 bits sin signo.</td>
</tr>
<tr class="odd">
<td>Doble</td>
<td>El valor debe ser un VT_R8, que es un doble.</td>
</tr>
<tr class="even">
<td>DateTime</td>
<td>El valor debe ser un VT_FILETIME, que es un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</td>
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
<td>Stream</td>
<td>El valor debe ser un VT_STREAM, que es un objeto que implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Portapapeles</td>
<td>El valor debe ser un VT_CF, que es un formato de Portapapeles.</td>
</tr>
<tr class="odd">
<td>Object</td>
<td>El valor debe ser un VT_UNKNOWN, que es un objeto que implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>Opcional. El valor predeterminado es &quot; discreto &quot; . Especifica cómo se muestra la propiedad cuando una vista está agrupada por esta propiedad. Una vez establecido aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>recupera estos valores. Los tipos válidos son los siguientes.

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
<td>Muestra los intervalos alfanuméricos estáticos para los valores.</td>
</tr>
<tr class="odd">
<td>Tamaño</td>
<td>Muestra los intervalos de tamaño estático de los valores.</td>
</tr>
<tr class="even">
<td>Fecha</td>
<td>Muestra los grupos de mes/año. Valor predeterminado para las propiedades de tipo = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Muestra en grupos relativos a tiempo.</td>
</tr>
<tr class="even">
<td>Dinámica</td>
<td>Muestra los intervalos creados dinámicamente para los valores.</td>
</tr>
<tr class="odd">
<td>Percent</td>
<td>Muestra los depósitos de porcentaje.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si la propiedad se considera innate. Una propiedad INNATE es aquella que se calcula a partir del contenido de un archivo o de otros recursos o sistemas. Por ejemplo, System. size es una propiedad INNATE proporcionada por el sistema de archivos; cambiar el valor de la propiedad en y de sí mismo no hace nada. Otros ejemplos son System. Image. Dimensions y System.Document. PageCount, que se calculan mediante programas basados en el contenido del archivo, no en función de una configuración modificable por el usuario. Establecer isInnate = &quot; true &quot; significa que el usuario no puede editar esta propiedad directamente a través de un control de propiedad. Este valor se asigna a la marca PDTF_ISINNATE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista con Service Pack 1 (SP1) y versiones posteriores</strong>. Público. Opcional. Cuando se establece en &quot; true &quot; , permite que se elimine una propiedad innate. Las propiedades de INNATE, que se calculan a partir de otras propiedades, son de solo lectura por definición. El valor predeterminado de este atributo depende del valor de <em>isInnate</em> .

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>Valor predeterminado de canBePurged</th>
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
Una propiedad cuyo valor <em>isInnate</em> es &quot; false &quot; (lo que significa que la propiedad es de lectura/escritura) no puede establecer también el valor de <em>canBePurged</em> en &quot; false &quot; . El sistema operativo aplica esta restricción.
</blockquote>
</div>
<div>
 
</div>
<p>Aunque este atributo se presentó en Windows Vista con Service Pack 1 (SP1), un archivo. propDesc que incluye este atributo es compatible con Windows vista antes de Windows Vista con SP1. El atributo <em>canBePurged</em> simplemente se omite en esa situación.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad puede tener varios valores. Este valor se asigna a la marca PDTF_MULTIPLEVALUES definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>. Esto también influye en si VT_VECTOR es o se va al VARTYPE del valor de propiedad.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si la propiedad es un encabezado de grupo. Un encabezado de grupo se usa estrictamente en Profiles, no tiene ningún valor, nunca se almacena en un archivo y también debe tener <typeInfo type=&quot;Null&quot;> . Parte de la interfaz de usuario del sistema usa los representadores para indicar la secuencia de las propiedades que se van a mostrar. Estos profiles pueden incluir referencias a los encabezados de grupo (por ejemplo, System. PropGroup. Camera), que indican a la interfaz de usuario que inicie una nueva sección de grupo (por ejemplo, &quot; configuración de cámara &quot; ). Una descripción de propiedad con isGroup = &quot; true &quot; debe especificar <labelInfo label=&quot;Some localized label&quot;> , de lo contrario, no es una propiedad útil. Este valor se asigna a la marca PDTF_ISGROUP definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>AggregationType</td>
<td>Público. Opcional. El valor predeterminado es &quot; default &quot; . Especifica cómo se muestran las propiedades de agregado cuando se seleccionan varios elementos. Una vez establecido aquí, <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: GetAggregationType</strong></a> recupera estos valores como <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Los tipos válidos son los siguientes.

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>Predeterminada. Muestra un marcador de posición de <strong>varios valores</strong> en la interfaz de usuario. Este es el valor predeterminado si el <em>tipo</em> es incompatible con el <em>aggregationType</em>especificado.</td>
</tr>
<tr class="even">
<td>First</td>
<td>Muestra el valor de propiedad del primer elemento de la selección o colección.</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Muestra la suma de los valores numéricos. Resulta útil para propiedades como System. Media. Duration o System. size. Este valor no es compatible con los tipos no numéricos.</td>
</tr>
<tr class="even">
<td>Average</td>
<td>Muestra el promedio de los valores numéricos. Resulta útil para las propiedades como System. Rating. Este valor no es compatible con los tipos no numéricos.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Muestra un intervalo de fechas. Resulta útil para propiedades como System. Photo. DateTaken. Este valor no es compatible con nada excepto Type = &quot; DateTime &quot; y es el valor predeterminado para las propiedades de ese tipo.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Muestra una Unión de todos los valores de la selección o la colección. El orden en que se muestran los valores es indefinido. Este valor es el predeterminado para las propiedades de tipo = &quot; String &quot; y multipleValues = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Máxima</td>
<td>Muestra el valor máximo de la colección. Útil para propiedades como System. DateModified. No es compatible con tipos no numéricos o sin fecha.</td>
</tr>
<tr class="even">
<td>Mínima</td>
<td>Muestra el valor mínimo de la colección. No es compatible con tipos no numéricos o sin fecha.</td>
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
<td>Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad está pensada para ser visible para el usuario. Por ejemplo, la interfaz de usuario del selector de columnas solo muestra las propiedades que tienen isViewable = &quot; true &quot; . La excepción es una interfaz de usuario controlada por un proplist, que siempre mostrará la propiedad. Si tiene una propiedad que solo está diseñada para el control de datos entre dos objetos y nunca está prevista su visualización por parte del usuario, este atributo debe ser false. Este valor se asigna a la marca PDTF_ISVIEWABLE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>Solo Windows Vista. No se admite en Windows 7 y versiones posteriores. Público. Opcional. El valor predeterminado es &quot;false&quot;. Especifica si esta propiedad está pensada para estar disponible en la interfaz de usuario de Generador de consultas de búsqueda. Una propiedad debe tener isViewable = &quot; true &quot; antes de que &quot; se respete isQueryable = true &quot; . Este valor se asigna a la marca PDTF_ISQUERYABLE definida en <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> y se usa en <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 y versiones posteriores.</strong> Público. Opcional. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Solo Windows Vista. No se admite en Windows 7 y versiones posteriores. Público. Opcional. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Público. Opcional. El valor predeterminado es &quot; String &quot; . Especifica una sugerencia para la interfaz de usuario de Generador de consultas de búsqueda para que pueda determinar la lista de posibles operadores de condición dentro de un predicado. A continuación se indican los valores reconocidos. 
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
<td>Predeterminada. Se usarán los siguientes operadores: &quot; es &quot; , &quot; no es &quot; , &quot; &lt; &quot; , &quot; &gt; &quot; , &quot; <= &quot; , &quot; >= &quot; , &quot; comienza con &quot; , &quot; termina con &quot; , &quot; contiene &quot; , &quot; no contiene &quot; , &quot; como &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Valor predeterminado para las propiedades numéricas. Se usarán los siguientes operadores: es igual a, no es igual a, &quot; &quot; &quot; &quot; &quot; es menor que &quot; , &quot; es mayor que &quot; , &quot; es menor o igual que &quot; , &quot; es mayor o igual que &quot; .</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Valor predeterminado para las propiedades de tipo = &quot; DateTime &quot; . Se usarán los siguientes operadores: &quot; is &quot; , &quot; is not &quot; , &quot; is Before, &quot; &quot; is After &quot; , &quot; is Before pero includes &quot; , &quot; is After y includes &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Valor predeterminado para las propiedades de tipo = &quot; booleano &quot; . Igual que el número.</td>
</tr>
<tr class="odd">
<td>Tamaño</td>
<td>Igual que el número.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Público. Opcional. El valor predeterminado es &quot; igual a &quot; . Especifica una sugerencia a la herramienta de Generador de consultas de búsqueda para que pueda determinar el operador predeterminado. Los valores posibles son los siguientes:

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Equal</td>
<td>Predeterminada. Indica un equivalente.</td>
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
<td>Valor predeterminado para las propiedades de conditionType = &quot; size &quot; . Indica mayor que.</td>
</tr>
<tr class="odd">
<td>Contiene</td>
<td>Valor predeterminado para las propiedades de conditionType = &quot; String &quot; . Indica la inclusión.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
