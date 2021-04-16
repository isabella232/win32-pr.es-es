---
description: Contiene un mapa de bits con codificación Base64 de una marca asociada a la sección de una nota de Journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705703"
---
# <a name="flag-element"></a>Elemento Flag

Contiene un mapa de bits con codificación Base64 de una marca asociada a la sección de una nota de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**Groupnode BizTalk**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                       |
|--------------|-------------------------------------------------------|
| Tipo de elemento | [**FlagType**](flagtype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink            |
| Nombre del esquema  | Lector de diario                                        |



 

 

 



