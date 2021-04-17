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
# <a name="record-attribute-schema"></a><span data-ttu-id="21b72-103">Esquema de atributo de registro</span><span class="sxs-lookup"><span data-stu-id="21b72-103">Record Attribute Schema</span></span>

<span data-ttu-id="21b72-104">Los registros pueden tener atributos específicos de la aplicación que son una secuencia de pares nombre-valor que se representan como una cadena XML en el miembro **pszAttributes** de la estructura del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="21b72-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="21b72-105">Los atributos se usan para filtrar una búsqueda de registros iniciada por llamadas a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), que toma un filtro de búsqueda XML especificado en el [formato de consulta de búsqueda de registros](record-search-query-format.md) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="21b72-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="21b72-106">Un atributo de registro puede ser uno de los tres tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="21b72-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="21b72-107">**int** es un valor entero.</span><span class="sxs-lookup"><span data-stu-id="21b72-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="21b72-108">**Date** es un valor de fecha y hora que se representa como uno de los formatos estándar descritos en [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="21b72-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="21b72-109">**String** es un valor de cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="21b72-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="21b72-110">La lista siguiente identifica los nombres de atributo específicos que están reservados por la infraestructura del mismo nivel:</span><span class="sxs-lookup"><span data-stu-id="21b72-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="21b72-111">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="21b72-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="21b72-112">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="21b72-112">**peercreatorid**</span></span>
-   <span data-ttu-id="21b72-113">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="21b72-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="21b72-114">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="21b72-114">**peerrecordid**</span></span>
-   <span data-ttu-id="21b72-115">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="21b72-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="21b72-116">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="21b72-116">**peercreationtime**</span></span>
-   <span data-ttu-id="21b72-117">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="21b72-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="21b72-118">Ejemplo de definición de atributos de registro</span><span class="sxs-lookup"><span data-stu-id="21b72-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="21b72-119">En el siguiente ejemplo de esquema se muestra cómo definir atributos de registro:</span><span class="sxs-lookup"><span data-stu-id="21b72-119">The following schema example shows you how to define record attributes:</span></span>

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
> <span data-ttu-id="21b72-120">Los nombres de atributo deben ser secuencias de caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="21b72-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="21b72-121">No se permiten caracteres especiales como guiones ("-") y caracteres de subrayado (" \_ ") en un nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="21b72-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="21b72-122">El siguiente ejemplo de una secuencia de atributo XML contiene los atributos de **AuthenticationType** y **AuthExpires** personalizados que aparecen en el miembro **PszAttributes** del [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span><span class="sxs-lookup"><span data-stu-id="21b72-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



