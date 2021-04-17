---
description: Contiene información sobre una palabra de tinta determinada en la nota de Journal, incluida la posición, los alternativos y los datos de tinta reales.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706508"
---
# <a name="inkword-element"></a>Elemento InkWord

Contiene información sobre una palabra de tinta determinada en la nota de Journal, incluida la posición, los alternativos y los datos de tinta reales.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Groupnode BizTalk**](groupnode-element.md)

[**Línea**](line-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Confianza**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

> [!WARNING]
> La asignación de coordenadas interna de la palabra de tinta es una unidad de métricas en inglés y la aplicación debe usar un multiplicador de 2,54 para convertir los valores de ancho y alto en las unidades de HIMETRIC utilizadas por las API de la plataforma de Tablet PC.

 

## <a name="element-information"></a>Información de elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**InkWordType**](inkwordtype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 



