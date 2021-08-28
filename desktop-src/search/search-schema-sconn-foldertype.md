---
description: El &lt; elemento folderType &gt; especifica guid para el tipo de carpeta. Este elemento es necesario si existe &lt; el &gt; elemento templateInfo. No tiene atributos ni elementos secundarios.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: elemento folderType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b693a1ff7007e6d63e108d16abe77ee421b3821a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882466"
---
# <a name="foldertype-element-search-connector-schema"></a>elemento folderType (esquema del conector de búsqueda)

El &lt; elemento folderType &gt; especifica guid para el tipo de carpeta. Este elemento es necesario si existe &lt; el &gt; elemento templateInfo. No tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax


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
| [elemento templateInfo (esquema del conector de búsqueda)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Comentarios

El GUID predeterminado es {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un tipo de carpeta general para conectores de búsqueda federada (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Ejemplo de un elemento folderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



