---
description: Recupera el tipo del trazo especificado.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer:: GetStrokeType (método) (IACom. h)'
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
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275465"
---
# <a name="iinkanalyzergetstroketype-method"></a>IInkAnalyzer:: GetStrokeType (método)

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

*lStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*pStrokeType* \[ enuncia\]
</dt> <dd>

La clasificación del trazo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) StrokeType sin \_ clasificar, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta. De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.

[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta. Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).

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

[**IInkAnalyzer:: SetStrokeType (método)**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**IInkAnalyzer:: SetStrokesType (método)**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




