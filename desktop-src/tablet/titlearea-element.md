---
description: Contiene la ubicación y la información de límite de la nota Title, si está presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f95c06e6aabe7c73cdc02a7fdb66c60f220adfbe72ea565b73cbc2c3f1a88bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589315"
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



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|   Elemento    | Value                                                           |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**TitleAreaType**](titleareatype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

 

 



