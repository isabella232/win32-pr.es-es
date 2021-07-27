---
description: Define un grupo de atributos utilizado por diversos elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento del documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Grupo de atributos BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c51fcb9bc0041bbc030f2c67e434a964212562
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436520"
---
# <a name="boundstype-attribute-group"></a>Grupo de atributos BoundsType

Define un grupo de atributos utilizado por diversos elementos de un archivo XML de diario. Contiene atributos que se usan para definir los límites (izquierda, superior, alto y ancho) de un elemento del documento.

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
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento.<br/> | Cualquier número entero.<br/>              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.<br/>  | Cualquier número entero.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.<br/>                                          | Cualquier entero no negativo.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.<br/>                                         | Cualquier entero no negativo.<br/> |



 

## <a name="type-information"></a>Información de tipo



|                 | Value                                      |
|-----------------|--------------------------------------------|
| **Espacio de nombres**   | urn:schemas-microsoft-com:tabletpc:richink |
| **Nombre del esquema** | Lector de diario                             |



 

## <a name="remarks"></a>Observaciones

**Left** y **Top** pueden ser negativos porque el origen está definido por los márgenes, no por la página.

 

 




