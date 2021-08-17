---
description: El <folderType> elemento especifica guid para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe. No tiene atributos ni elementos secundarios.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: elemento folderType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6b9d5682a85126a467c051b9f1103a4ac10f2f6936cc24dd4438a5f8c75d44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862604"
---
# <a name="foldertype-element-search-connector-schema"></a>elemento folderType (esquema del conector de búsqueda)

El <folderType> elemento especifica guid para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe. No tiene atributos ni elementos secundarios.

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



 

 



