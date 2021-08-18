---
description: Recupera el tipo del trazo especificado.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: Método IInkAnalyzer::GetStrokeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71bf3775be1c21e59cf41a51fa5a6140e86e44ac81a2863892c1f252666e0f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092145"
---
# <a name="iinkanalyzergetstroketype-method"></a>IInkAnalyzer::GetStrokeType (método)

Recupera el tipo del trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*pStrokeType* \[ out\]
</dt> <dd>

Clasificación del trazo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si el tipo del trazo es el valor [**StrokeType**](stroketype.md) StrokeType \_ Unclassified, [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de lápiz. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor del tipo de trazo como parte del análisis de lápiz. Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer::SetStrokeType o**](iinkanalyzer-setstroketype.md) el método [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokeType (Método)**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesType (Método)**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




