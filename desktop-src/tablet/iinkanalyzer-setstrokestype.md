---
description: Cambia el tipo de los trazos especificados.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: Método IInkAnalyzer::SetStrokesType (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572384"
---
# <a name="iinkanalyzersetstrokestype-method"></a>IInkAnalyzer::SetStrokesType (método)

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

*strokeIdCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de trazo de los trazos a los que se va a asignar *StrokeType.*

</dd> <dt>

*StrokeType* \[ En\]
</dt> <dd>

Valor [**strokeType**](stroketype.md) que se asignará a los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Si el tipo del trazo es el valor [**StrokeType**](stroketype.md) **StrokeType \_ Unclassified**, [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de lápiz. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor del tipo de trazo como parte del análisis de lápiz. Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer::SetStrokeType o**](iinkanalyzer-setstroketype.md) el método **IInkAnalyzer::SetStrokesType**.

Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar (vea [**IContextNode::GetType),**](icontextnode-gettype.md)este método mueve el trazo a un nodo de entrada de lápiz sin clasificar que contiene trazos del mismo lenguaje. Si no existe ningún nodo de contexto, este método crea un nuevo nodo de entrada de lápiz sin clasificar y le agrega el trazo. Un nodo de entrada de lápiz sin clasificar es **un IContextNode** de tipo UnclassifiedInk.

Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar, este método también agrega el rectángulo delimitador del trazo a la región desusada del analizador de entrada de lápiz (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el *parámetro StrokeType* coincide con el tipo actual del trazo.

Si un trazo identificado en *strokeIds* no está asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método omite el identificador.

Si ninguno de los trazos especificados identifica un trazo asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método devuelve sin actualizar **IInkAnalyzer**.

Al establecer el tipo de trazo en los trazos asociados a un ContextNode que tiene NodeTypeAndProperties confirmado, se genera una excepción InvalidOperationException.

Este método devuelve un código de error cuando *plStrokes* es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::GetStrokeType (Método)**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokeType (Método)**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




