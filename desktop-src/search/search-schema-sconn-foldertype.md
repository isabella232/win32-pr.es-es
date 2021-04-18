---
description: El <folderType> elemento especifica el GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe. No tiene atributos ni elementos secundarios.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento folderType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497056"
---
# <a name="foldertype-element-search-connector-schema"></a>Elemento folderType (esquema del conector de búsqueda)

El <folderType> elemento especifica el GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe. No tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Sintaxis


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                         | Elementos secundarios |
|----------------------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (esquema del conector de búsqueda)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Observaciones

El GUID predeterminado es {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un tipo de carpeta general para conectores de búsqueda federada (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Ejemplo de un elemento folderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



