---
description: Este &lt; elemento searchConnectorDescriptionList contiene una lista de conectores de búsqueda que se asignan &gt; a ubicaciones incluidas en esta biblioteca. Cada conector de búsqueda se define mediante un &lt; elemento searchConnectorDescription. &gt; Este elemento es opcional y no tiene atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885611"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>elemento searchConnectorDescriptionList (esquema de biblioteca)

Este &lt; elemento searchConnectorDescriptionList contiene una lista de conectores de búsqueda que se asignan &gt; a ubicaciones incluidas en esta biblioteca. Cada conector de búsqueda se define mediante un &lt; elemento searchConnectorDescription. &gt; Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Comentarios

Los conectores de búsqueda Windows ámbitos de controlador de protocolo y búsqueda federada no se pueden incluir en una biblioteca.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
