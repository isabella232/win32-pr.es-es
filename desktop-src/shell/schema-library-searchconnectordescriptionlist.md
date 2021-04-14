---
description: Este <searchConnectorDescriptionList> elemento contiene una lista de conectores de búsqueda que se asignan a ubicaciones incluidas en esta biblioteca. Cada conector de búsqueda se define mediante un <searchConnectorDescription> elemento. Este elemento es opcional y no tiene atributos.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985891"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>Elemento searchConnectorDescriptionList (esquema de biblioteca)

Este <searchConnectorDescriptionList> elemento contiene una lista de conectores de búsqueda que se asignan a ubicaciones incluidas en esta biblioteca. Cada conector de búsqueda se define mediante un <searchConnectorDescription> elemento. Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Sintaxis

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
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Observaciones

Los conectores de búsqueda para los ámbitos de búsqueda federada de Windows y de controlador de Protocolo no se pueden incluir en una biblioteca.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
