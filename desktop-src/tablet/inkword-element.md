---
description: Contiene información sobre una palabra de entrada de lápiz determinada en la nota de diario, incluida la posición, las alternativas y los datos de entrada de lápiz reales.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342da6688088d37065af7af8600ac2e1e7003599914b320b21e49d39235dc712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717324"
---
# <a name="inkword-element"></a>Elemento InkWord

Contiene información sobre una palabra de entrada de lápiz determinada en la nota de diario, incluida la posición, las alternativas y los datos de entrada de lápiz reales.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**GroupNode**](groupnode-element.md)

[**Línea**](line-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Confianza**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite para el elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite para el elemento.                                         | Cualquier entero no negativo. |



 

> [!WARNING]
> La asignación de coordenadas internas de la palabra manuscrita es Unidades métricas en inglés y la aplicación deberá usar un multiplicador de 2,54 para convertir los valores width y height en las unidades HIMETRIC que usan las API de la plataforma de Tablet PC.

 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**InkWordType**](inkwordtype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 



