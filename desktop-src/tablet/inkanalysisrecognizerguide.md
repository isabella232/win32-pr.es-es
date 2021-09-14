---
description: Especifica la guía o el área donde se dibuja y reconoce la entrada de lápiz.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Estructura InkAnalysisRecognizerGuide (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251901"
---
# <a name="inkanalysisrecognizerguide-structure"></a>InkAnalysisRecognizerGuide (estructura)

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



## <a name="members"></a>Members

<dl> <dt>

**rectWritingBox**
</dt> <dd>

El área de escritura invisible de la guía de reconocimiento en la que realmente puede tener lugar la escritura.

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

Rectángulo que se dibuja en la pantalla de tableta y en el que tiene lugar la escritura.

</dd> <dt>

**Cuervos**
</dt> <dd>

Número de filas del cuadro de la guía de reconocimiento.

</dd> <dt>

**cColumns**
</dt> <dd>

Número de columnas del cuadro de la guía de reconocimiento.

</dd> <dt>

**Midline**
</dt> <dd>

Alto de línea media del cuadro de guía de reconocimiento. El alto de la línea media es la distancia desde la línea base hasta la línea media del cuadro dibujado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**InkAnalysisRecognizerGuide** define un área de entrada esperada, como una línea o cuadros, para los caracteres. Una **estructura InkAnalysisRecognizerGuide** solo se puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode::GetType).**](icontextnode-gettype.md) [**IInkAnalyzer**](iinkanalyzer.md) usa la ubicación del nodo de sugerencias de análisis y las ubicaciones de los trazos de lápiz para asociar un trazo al nodo de sugerencia de análisis. Los trazos con una asociación al nodo de sugerencias de análisis tendrán el **inkAnalysisRecognizerGuide** especificado usado cuando lo reconozca un **IInkAnalyzer,** siempre que **IInkAnalyzer** admita **InkAnalysisRecognizerGuide**. Los valores expresados en la **clase InkAnalysisRecognizerGuide** siempre son relativos a la ubicación del nodo de sugerencias de análisis y se especifican en coordenadas de espacio de entrada de lápiz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de sugerencias de análisis](analysis-hint-properties.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




