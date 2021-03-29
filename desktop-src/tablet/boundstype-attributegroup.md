---
description: Define un grupo de atributos que se utiliza en una variedad de elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento en el documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807981"
---
# <a name="boundstype-attribute-group"></a>Grupo de atributos BoundsType

Define un grupo de atributos que se utiliza en una variedad de elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento en el documento.

## <a name="definition"></a>Definición

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.<br/> | Cualquier número entero.<br/>              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.<br/>  | Cualquier número entero.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.<br/>                                          | Cualquier entero no negativo.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.<br/>                                         | Cualquier entero no negativo.<br/> |



 

## <a name="type-information"></a>Información de tipo



|             |                                            |
|-------------|--------------------------------------------|
| Espacio de nombres   | urn: schemas-microsoft-com: TabletPC: richink |
| Nombre del esquema | Lector de diario                             |



 

## <a name="remarks"></a>Observaciones

**Left** y **Top** pueden ser negativos porque el origen está definido por los márgenes, no por la página.

 

 




