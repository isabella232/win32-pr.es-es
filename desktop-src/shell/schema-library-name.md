---
description: El <name> elemento especifica el nombre de esta biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: name (Elemento, Esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883945"
---
# <a name="name-element-library-schema"></a>name (Elemento, Esquema de biblioteca)

El <name> elemento especifica el nombre de esta biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentarios

El nombre es el nombre descriptivo de la biblioteca que se muestra en Windows Explorer. El nombre se puede especificar en un formato <dllname> , como en el ejemplo <index> siguiente.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
