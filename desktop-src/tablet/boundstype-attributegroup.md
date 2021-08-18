---
description: Define un grupo de atributos utilizado por diversos elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, parte superior, alto y ancho) de un elemento del documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba91269660875e55b92797609969ebee38d221016914d9473cd5eddd245cfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967774"
---
# <a name="boundstype-attribute-group"></a>Grupo de atributos BoundsType

Define un grupo de atributos utilizado por diversos elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, parte superior, alto y ancho) de un elemento del documento.

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



| Atributo  | Tipo                      | Requerido | Descripción                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento.<br/> | Cualquier número entero.<br/>              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.<br/>  | Cualquier número entero.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.<br/>                                          | Cualquier entero no negativo.<br/> |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.<br/>                                         | Cualquier entero no negativo.<br/> |



 

## <a name="type-information"></a>Información de tipo



|                 | Value                                      |
|-----------------|--------------------------------------------|
| **Espacio de nombres**   | urn:schemas-microsoft-com:tabletpc:richink |
| **Nombre del esquema** | Lector de diario                             |



 

## <a name="remarks"></a>Comentarios

**Left** y **Top** pueden ser negativos porque el origen está definido por los márgenes, no por la página.

 

 




