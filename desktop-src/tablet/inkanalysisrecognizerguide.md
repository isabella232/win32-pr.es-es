---
description: Especifica la guía o el área donde se dibuja y reconoce la entrada de lápiz.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Estructura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696338"
---
# <a name="inkanalysisrecognizerguide-structure"></a>Estructura InkAnalysisRecognizerGuide

Especifica la guía o el área donde se dibuja y reconoce la entrada de lápiz.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>Miembros

<dl> <dt>

**rectWritingBox**
</dt> <dd>

Área de escritura invisible de la guía de reconocimiento en la que realmente se puede realizar la escritura.

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

Rectángulo que se dibuja en la pantalla de Tablet PC y en el que tiene lugar la escritura.

</dd> <dt>

**cRows**
</dt> <dd>

El número de filas en el cuadro guía de reconocimiento.

</dd> <dt>

**cColumns**
</dt> <dd>

El número de columnas en el cuadro guía de reconocimiento.

</dd> <dt>

**Elips**
</dt> <dd>

El alto de la media en el cuadro de la guía de reconocimiento. El alto de línea media es la distancia desde la línea de base hasta la línea media del cuadro dibujado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un **InkAnalysisRecognizerGuide** define un área esperada de entrada, como una línea o cuadros, para los caracteres. Una estructura **InkAnalysisRecognizerGuide** solo se puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)). [**IInkAnalyzer**](iinkanalyzer.md) usa la ubicación del nodo de sugerencia de análisis y las ubicaciones de los trazos de entrada de lápiz para asociar un trazo al nodo de sugerencia de análisis. Los trazos con una asociación al nodo de sugerencia de análisis tendrán el **InkAnalysisRecognizerGuide** especificado que se usará cuando lo reconozca un **IInkAnalyzer**, siempre que el **IInkAnalyzer** admita **InkAnalysisRecognizerGuide**. Los valores expresados en la clase **InkAnalysisRecognizerGuide** siempre se relacionan con la ubicación del nodo de sugerencia de análisis y se especifican en coordenadas de espacio de tinta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la sugerencia de análisis](analysis-hint-properties.md)
</dt> <dt>

[**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




