---
description: Cambia el tipo de los trazos especificados.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'IInkAnalyzer:: SetStrokesType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715201"
---
# <a name="iinkanalyzersetstrokestype-method"></a>IInkAnalyzer:: SetStrokesType (método)

Cambia el tipo de los trazos especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strokeIdCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ de\]
</dt> <dd>

Una matriz que contiene los identificadores de trazo de los trazos a los que se asigna *StrokeType*.

</dd> <dt>

*StrokeType* \[ de\]
</dt> <dd>

Valor de [**StrokeType**](stroketype.md) que se va a asignar a los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) **StrokeType sin \_ clasificar**, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta. Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o **IInkAnalyzer:: SetStrokesType**.

Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)), este método mueve el trazo a un nodo de tinta sin clasificar que contiene trazos del mismo idioma. Si no existe tal nodo de contexto, este método crea un nuevo nodo de entrada sin clasificar y le agrega el trazo. Un nodo de tinta sin clasificar es un **IContextNode** de tipo UnclassifiedInk.

Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de tinta no clasificado, este método también agrega el rectángulo de selección del trazo a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el parámetro *StrokeType* coincide con el tipo actual del trazo.

Si un trazo identificado en *strokeIds* no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.

Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

Al establecer el tipo de trazo en los trazos que están asociados a un ContextNode que tiene NodeTypeAndProperties confirmada, se producirá una excepción InvalidOperationException.

Este método devuelve un código de error cuando *plStrokes* es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: GetStrokeType (método)**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer:: SetStrokeType (método)**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




