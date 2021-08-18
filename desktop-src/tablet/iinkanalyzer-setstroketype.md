---
description: Cambia el tipo del trazo especificado.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: Método IInkAnalyzer::SetStrokeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6d65c01ba3618bad563ee2b8c8a9c4fee3479a12c796b2f2f570832fac1d826c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709035"
---
# <a name="iinkanalyzersetstroketype-method"></a>IInkAnalyzer::SetStrokeType (método)

Cambia el tipo del trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ En\]
</dt> <dd>

Identificador de trazo del trazo al que se va a asignar *StrokeType.*

</dd> <dt>

*StrokeType* \[ En\]
</dt> <dd>

Valor [**strokeType**](stroketype.md) que se asignará al trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si el tipo del trazo es el valor [**StrokeType**](stroketype.md) **StrokeType \_ Unclassified**, [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de lápiz. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor del tipo de trazo como parte del análisis de lápiz. Para especificar o cambiar el tipo de trazo, use el método **IInkAnalyzer::SetStrokeType o** el método [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar (vea [**IContextNode::GetType),**](icontextnode-gettype.md)este método mueve el trazo a un nodo de entrada de lápiz sin clasificar que contiene trazos del mismo lenguaje. Si no existe ningún nodo de contexto, este método crea un nuevo nodo de entrada de lápiz sin clasificar y le agrega el trazo. Un nodo de entrada de lápiz sin clasificar es **un IContextNode** de tipo UnclassifiedInk.

Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar, este método también agrega el rectángulo delimitador del trazo a la región desusada del analizador de entrada de lápiz (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el *parámetro StrokeType* coincide con el tipo actual del trazo.

Al establecer el tipo de trazo en los trazos asociados a un ContextNode que tiene NodeTypeAndProperties confirmado, se genera una excepción InvalidOperationException.

Si el trazo especificado no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::GetStrokeType (Método)**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesType (Método)**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




