---
description: Contiene la ubicación y la información de límite de la nota Title, si está presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432197"
---
# <a name="titlearea-element"></a>Elemento TitleArea

Contiene la ubicación y la información de límite de la nota Title, si está presente.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Título**](title-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|   Elemento    | Value                                                           |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**TitleAreaType**](titleareatype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

 

 



