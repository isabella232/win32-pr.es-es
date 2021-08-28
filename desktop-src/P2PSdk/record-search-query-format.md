---
description: Una llamada a la función PeerGroupSearchRecords requiere un parámetro de cadena de consulta XML que se usa para determinar los criterios básicos de una búsqueda.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Formato de consulta de búsqueda de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a130d937177d4f903bfe52b121b2d67f8720d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887004"
---
# <a name="record-search-query-format"></a>Formato de consulta de búsqueda de registros

Una llamada a la [**función PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) requiere un parámetro de cadena de consulta XML que se usa para determinar los criterios básicos de una búsqueda. Use el esquema siguiente para formular una cadena XML:

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

### <a name="elements-to-use-for-a-record-search"></a>Elementos que se usarán para una búsqueda de registros

El elemento principal de una búsqueda de registros es **peersearch**, que contiene el identificador uniforme de recursos (URI) del esquema asociado en el **atributo xmlns.** Cuando **peersearch** se usa como elemento secundario, puede usar **y**, **cláusula** y **o como** elementos secundarios.

-   **y** : el **elemento y** realiza una operación AND lógica en una o varias cláusulas contenidas entre las etiquetas de apertura y cierre. Otras **etiquetas** **y o** pueden ser elementos secundarios, y los resultados recursivos de sus cláusulas secundarias se incluyen en la operación.

    Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters y una última actualización mayor que 2/28/2003, o una fecha de creación menor que 1/31/2003, use la siguiente cadena de consulta XML:

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

-   **clause:** el **elemento clause** especifica una regla comparativa básica que compara el valor de un atributo de registro específico con el valor contenido entre las etiquetas de apertura y cierre. El **tipo** y **los atributos de** comparación que se deben proporcionar **comparan** indica la operación de comparación que se va a realizar. Por ejemplo, una búsqueda simple que indica que todos los registros coincidentes deben tener un valor **peercreatorid** igual a James Peters aparece en la cadena de consulta XML de la siguiente manera:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Los **atributos de** tipo comunes incluyen **int**, **string** y **date**. El **atributo date** puede ser uno de los formatos de fecha estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Los valores del **atributo compare** son **iguales,** **notequal,** **less,** **greater,** **lessorequal** y **greaterorequal.**

<!-- -->

-   **o** : el **elemento o** realiza una operación LÓGICA OR en una o varias cláusulas contenidas entre las etiquetas de apertura y cierre. Otros **elementos** o **y pueden** ser elementos secundarios, y los resultados recursivos de las cláusulas secundarias se incluyen en la operación. Por ejemplo, si desea obtener un registro que contenga un nombre igual a James Peters, o una última actualización que esté entre 31/1/2003 y 2/28/2003, use la siguiente cadena de consulta XML:

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

## <a name="more-information-about-a-record-search"></a>Más información sobre una búsqueda de registros

El primer nivel de nodos después **de peersearch** solo puede tener un elemento. Sin embargo, los elementos secundarios posteriores de ese elemento pueden tener muchos elementos en el mismo nivel.

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

Se produce un error en la consulta porque se devuelven dos valores para la coincidencia sin resolverse en un valor true/false, lo que significa que una cláusula es una consulta para el nombre de un registro que es igual a James Peters, y la operación AND coincide con las dos cláusulas de componente. El resultado son dos valores true/false lógicos que son contradictorios.

Para obtener todos los registros que contienen un nombre igual a James Peters y una última actualización que esté entre el 31/1/2003 y el 2/28/2003, coloque la cláusula y las etiquetas y que están en el mismo nivel entre apertura **y** cierre y etiquetas.   En el ejemplo siguiente se muestra la consulta correcta:

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

En la lista siguiente se identifica otra información específica que debe conocer para escribir una consulta correcta:

-   Las  etiquetas y y o no  se pueden encontrar entre las etiquetas de la cláusula de apertura y cierre porque, en esa configuración, se interpretan como parte del valor con el que se debe coincidir, lo que produce un error o una coincidencia con errores. 
-   Cada par de **etiquetas de** **apertura** y o de apertura y cierre debe incluir al menos uno o varios nodos secundarios.
-   No se permite un conjunto cero de elementos en este esquema.

## <a name="record-attributes"></a>Atributos de registro

Mediante el esquema [de atributo de registro](record-attribute-schema.md), un usuario puede crear atributos de registro que especifica el atributo XML **attrib** en un elemento de cláusula. Los atributos de un nuevo registro se agregan estableciendo el miembro **pszAttributes** de [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) en una cadena XML con el formato especificado en el esquema.

La infraestructura del mismo nivel reserva los siguientes nombres de atributo:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caracteres especiales

Ciertos caracteres se pueden usar para expresar patrones de coincidencia o para escapar otros caracteres especiales. Estos caracteres se describen en la tabla siguiente. 

| Patrón de caracteres | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Carácter comodín. Cuando este carácter se encuentra en un valor de cláusula, coincide con 0-n caracteres de cualquier valor, incluidos los espacios en blanco y los caracteres no alfanuméricos. Por ejemplo:<br/> " <clause attrib="peercreatorid" type="string" compare="equal"> James P \* &lt; /clause &gt; "<br/> Esta cláusula coincide con **todos los valores peercreatorid** con un nombre de "James" y un apellido que empieza por "P".<br/> |
| \\\*              | Asterisco de escape. Esta secuencia coincide con un carácter de asterisco.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Carácter comodín de un solo carácter. Cuando este carácter se encuentra en un valor de cláusula, coincide con cualquier carácter individual, incluidos los espacios en blanco y los caracteres no alfanuméricos. Por ejemplo:<br/> " <clause attrib="filename" type="string" compare="equal"> data-0?.xml&lt; /clause &gt; "<br/> Esta cláusula coincide **con valores de** nombre de archivo como "data-01.xml" y "data-0B.xml".<br/>                              |
| \\?               | Signo de interrogación con escape. Esta secuencia coincide con un carácter de signo de interrogación.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Barra diagonal inversa con escape. Esta secuencia coincide con un único carácter de barra diagonal inversa.                                                                                                                                                                                                                                                                                                                                                               |



 

Si la secuencia de caracteres no es válida, la [**función PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) devuelve el error **E \_ INVALIDARG**. Una secuencia no válida es cualquier secuencia que contiene un carácter " " (barra diagonal inversa) no seguido inmediatamente de un \\ carácter " \* " (asterisco), un "?" (signo de interrogación) u otro carácter \\ " " (barra diagonal inversa).

 

 




