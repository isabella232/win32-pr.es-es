---
description: Los registros pueden tener atributos específicos de la aplicación que son una secuencia de pares nombre-valor que se representan como una cadena XML en el miembro pszAttributes de la estructura del registro del mismo nivel \_ .
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Esquema de atributo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668355"
---
# <a name="record-attribute-schema"></a>Esquema de atributo de registro

Los registros pueden tener atributos específicos de la aplicación que son una secuencia de pares nombre-valor que se representan como una cadena XML en el miembro **pszAttributes** de la estructura del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Los atributos se usan para filtrar una búsqueda de registros iniciada por llamadas a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), que toma un filtro de búsqueda XML especificado en el [formato de consulta de búsqueda de registros](record-search-query-format.md) como parámetro.

Un atributo de registro puede ser uno de los tres tipos siguientes:

-   **int** es un valor entero.
-   **Date** es un valor de fecha y hora que se representa como uno de los formatos estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **String** es un valor de cadena Unicode.

La lista siguiente identifica los nombres de atributo específicos que están reservados por la infraestructura del mismo nivel:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Ejemplo de definición de atributos de registro

En el siguiente ejemplo de esquema se muestra cómo definir atributos de registro:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> Los nombres de atributo deben ser secuencias de caracteres alfanuméricos. No se permiten caracteres especiales como guiones ("-") y caracteres de subrayado (" \_ ") en un nombre de atributo.

 

El siguiente ejemplo de una secuencia de atributo XML contiene los atributos de **AuthenticationType** y **AuthExpires** personalizados que aparecen en el miembro **PszAttributes** del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



