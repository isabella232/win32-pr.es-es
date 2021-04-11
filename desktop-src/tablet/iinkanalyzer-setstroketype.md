---
description: Cambia el tipo del trazo especificado.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer:: SetStrokeType (método) (IACom. h)'
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
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154405"
---
# <a name="iinkanalyzersetstroketype-method"></a>IInkAnalyzer:: SetStrokeType (método)

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

*lStrokeId* \[ de\]
</dt> <dd>

Identificador de trazo del trazo al que se va a asignar *StrokeType*.

</dd> <dt>

*StrokeType* \[ de\]
</dt> <dd>

Valor de [**StrokeType**](stroketype.md) que se va a asignar al trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) **StrokeType sin \_ clasificar**, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta. Para especificar o cambiar el tipo de trazo, use el método **IInkAnalyzer:: SetStrokeType** o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).

Si un trazo está asociado a un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)), este método mueve el trazo a un nodo de tinta sin clasificar que contiene trazos del mismo idioma. Si no existe tal nodo de contexto, este método crea un nuevo nodo de entrada sin clasificar y le agrega el trazo. Un nodo de tinta sin clasificar es un **IContextNode** de tipo UnclassifiedInk.

Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de tinta no clasificado, este método también agrega el rectángulo de selección del trazo a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el parámetro *StrokeType* coincide con el tipo actual del trazo.

Al establecer el tipo de trazo en los trazos que están asociados a un ContextNode que tiene NodeTypeAndProperties confirmada, se producirá una excepción InvalidOperationException.

Si el trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

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

[**IInkAnalyzer:: SetStrokesType (método)**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




