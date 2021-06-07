---
description: Contiene un mapa de bits codificado en Base64 de una marca asociada a la sección de una nota de diario.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432337"
---
# <a name="flag-element"></a>Elemento Flag

Contiene un mapa de bits codificado en Base64 de una marca asociada a la sección de una nota de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite para el elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite para el elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------|
| Tipo de elemento | [**FlagType**](flagtype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink            |
| Nombre del esquema  | Lector de diario                                        |



 

 

 



