---
description: Devuelve el identificador de configuración regional del trazo especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'IInkAnalyzer:: GetStrokeLanguageId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810003"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>IInkAnalyzer:: GetStrokeLanguageId (método)

Devuelve el identificador de configuración regional del trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*lStrokeLCID* \[ enuncia\]
</dt> <dd>

Identificador de configuración regional del trazo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

La configuración regional del trazo se establece al agregar el trazo mediante una llamada al método [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), el método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para cambiar la configuración regional del trazo, use el método [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

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

[**IInkAnalyzer:: SetStrokeLanguageId (método)**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer:: SetStrokesLanguageId (método)**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




