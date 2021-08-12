---
description: Los registros pueden tener atributos específicos de la aplicación que son una secuencia de pares de nombre o valor representados como una cadena XML en el miembro pszAttributes de la estructura PEER \_ RECORD.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Esquema de atributo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597369d7214b51b94a74b777315bb2ce2beb280232be5fb29571376ad3fc93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612316"
---
# <a name="record-attribute-schema"></a>Esquema de atributo de registro

Los registros pueden tener atributos específicos de la aplicación que son una secuencia de pares de nombre o valor representados como una cadena XML en el **miembro pszAttributes** de la [**estructura PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Los atributos se usan para filtrar una búsqueda de registros iniciada por llamadas a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), que toma un filtro de búsqueda XML especificado en [Formato](record-search-query-format.md) de consulta de búsqueda de registros como parámetro.

Un atributo de registro puede ser uno de los tres tipos siguientes:

-   **int** es un valor entero.
-   **date** es un valor datetime representado como uno de los formatos estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **string** es un valor de cadena Unicode.

En la lista siguiente se identifican los nombres de atributo específicos reservados por la infraestructura del mismo nivel:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Ejemplo de definición de atributos de registro

En el ejemplo de esquema siguiente se muestra cómo definir atributos de registro:

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

 

El ejemplo siguiente de una secuencia de atributos XML contiene los atributos **authenticationType** y **AuthExpires personalizados** que aparecen en el miembro **pszAttributes** de [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



