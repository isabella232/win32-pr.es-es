---
description: Una llamada a la función PeerGroupSearchRecords requiere un parámetro de cadena de consulta XML que se utiliza para determinar los criterios básicos de una búsqueda.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Formato de consulta de búsqueda de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911625"
---
# <a name="record-search-query-format"></a>Formato de consulta de búsqueda de registros

Una llamada a la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) requiere un parámetro de cadena de consulta XML que se utiliza para determinar los criterios básicos de una búsqueda. Use el esquema siguiente para formular una cadena XML:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a>Elementos que se van a usar para una búsqueda de registros

El elemento principal de una búsqueda de registros es **peersearch**, que contiene el identificador uniforme de recursos (URI) del esquema asociado en el atributo **xmlns** . Cuando **peersearch** se usa como un elemento secundario, puede usar los elementos **y**, la **cláusula** y **o** como elementos secundarios.

-   **y** : el elemento **y** realiza una operación and lógica en una o más cláusulas contenidas entre las etiquetas de apertura y cierre. Otras etiquetas **and** y **or** pueden ser elementos secundarios, y los resultados recursivos de sus cláusulas secundarias se incluyen en la operación.

    Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters y una última actualización mayor que 2/28/2003, o una fecha de creación inferior a 1/31/2003, use la siguiente cadena de consulta XML:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   **cláusula** : el elemento de la **cláusula** especifica una regla comparativa básica que compara el valor de un atributo de registro específico con el valor incluido entre las etiquetas de apertura y cierre. Se **deben proporcionar los** atributos **Type** y **Compare** para indicar la operación de comparación que se va a realizar. Por ejemplo, una búsqueda simple que indica que todos los registros coincidentes deben tener un valor de **peercreatorid** igual a James Peters aparece en la cadena de consulta XML como se indica a continuación:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Los atributos de **tipo** comunes son **int**, **String** y **Date**. El atributo **Date** puede ser uno de los formatos de fecha estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Los valores del atributo **Compare** son **Equal**, **notequal**, **less**, **Greater**, **lessorequal** y **greaterorequal**.

<!-- -->

-   **o** bien-el elemento **o** realiza una operación OR lógica en una o más cláusulas contenidas entre las etiquetas de apertura y cierre. Los elementos **o** y **y** pueden ser elementos secundarios, y los resultados recursivos de las cláusulas secundarias se incluyen en la operación. Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters, o una última actualización entre 1/31/2003 y 2/28/2003, use la siguiente cadena de consulta XML:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a>Más información acerca de una búsqueda de registros

El primer nivel de nodos después de **peersearch** solo puede tener un elemento. Sin embargo, los elementos secundarios posteriores de ese elemento pueden tener muchos elementos en el mismo nivel.

La siguiente consulta de búsqueda es incorrecta:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

Se produce un error en la consulta porque se devuelven dos valores para la coincidencia sin resolverse en un valor true/false, lo que significa que una cláusula es una consulta para el nombre de un registro que es igual a James Peters, y la operación y coincide con las dos cláusulas de componentes. El resultado son dos valores lógicos verdadero/falso que son contradictorios.

Para obtener todos los registros que contienen un nombre igual a James Peters y una última actualización entre 1/31/2003 y 2/28/2003, coloque la **cláusula** y las etiquetas que estén en el mismo nivel entre la apertura y el cierre **y** **las etiquetas.** En el ejemplo siguiente se muestra la consulta correcta:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

En la siguiente lista se identifica otra información específica que debe saber para escribir una consulta correcta:

-   Las etiquetas **and** y **or** no se pueden encontrar entre las etiquetas de la **cláusula** de apertura y de cierre porque, en esa configuración, se interpretan como parte del valor con el que debe coincidir, lo que genera un error o una coincidencia con errores.
-   Cada par de etiquetas **and** y **or** y de apertura y cierre deben incluir al menos uno o más nodos secundarios.
-   No se permite un conjunto de elementos cero en este esquema.

## <a name="record-attributes"></a>Atributos de registro

Mediante el uso del [esquema de atributo de registro](record-attribute-schema.md), un usuario puede crear atributos de registro que el atributo **attrib** XML de un elemento de la cláusula especifique. Los atributos de un nuevo registro se agregan estableciendo el miembro **pszAttributes** del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) en una cadena XML con el formato especificado en el esquema.

La infraestructura del mismo nivel reserva los siguientes nombres de atributo:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caracteres especiales

Algunos caracteres se pueden usar para expresar patrones de coincidencia o para aplicar un carácter de escape a otros caracteres especiales. Estos caracteres se describen en la tabla siguiente. 

| Patrón de caracteres | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Carácter comodín. Cuando este carácter se encuentra en un valor de la cláusula, coincide con 0-n caracteres de cualquier valor, incluidos los caracteres de espacio en blanco y no alfanuméricos. Por ejemplo:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"<br/> Esta cláusula coincide con todos los valores de **peercreatorid** con el nombre "James" y el apellido que empieza por "P".<br/> |
| \\\*              | Asterisco con escape. Esta secuencia coincide con un carácter de asterisco.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Carácter comodín de un solo carácter. Cuando este carácter se encuentra en un valor de la cláusula, coincide con cualquier carácter individual, incluidos los caracteres de espacio en blanco y no alfanuméricos. Por ejemplo:<br/> "<clause attrib="filename" type="string" compare="equal">Data-0?. XML</clause>"<br/> Esta cláusula coincide con los valores de **nombre de archivo** como "data-01.xml" y "data-0B.xml".<br/>                              |
| \\?               | Un signo de interrogación de escape. Esta secuencia coincide con un carácter de signo de interrogación.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Una barra diagonal inversa con escape. Esta secuencia coincide con un único carácter de barra diagonal inversa.                                                                                                                                                                                                                                                                                                                                                               |



 

Si la secuencia de caracteres no es válida, la función [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) devuelve el error **E \_ INVALIDARG**. Una secuencia no válida es cualquier secuencia que contenga un \\ carácter "" (barra diagonal inversa) no seguido inmediatamente de un \* carácter "" (asterisco), una "?" (signo de interrogación), u otro \\ carácter "" (barra diagonal inversa).

 

 




