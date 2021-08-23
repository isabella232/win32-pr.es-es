---
description: Devuelve el identificador de configuración regional del trazo especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: Método IInkAnalyzer::GetStrokeLanguageId (IACom.h)
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
ms.openlocfilehash: 8b61bfa61b4e4aa2c8415c9596cb97a3b0c1313cf3a080d065a7c82e4d69b84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713395"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>IInkAnalyzer::GetStrokeLanguageId (método)

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

*lStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*lStrokeLCID* \[ out\]
</dt> <dd>

Identificador de configuración regional para el trazo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

La configuración regional del trazo se establece cuando se agrega el trazo mediante una llamada al método [**IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md), al método [**IInkAnalyzer::AddStrokeForLanguage,**](iinkanalyzer-addstrokeforlanguage.md)al método [**IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)o al método [**IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para cambiar la configuración regional del trazo, use el método [**IInkAnalyzer::SetStrokeLanguageId o**](iinkanalyzer-setstrokelanguageid.md) el método [**IInkAnalyzer::SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokeLanguageId (Método)**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesLanguageId (Método)**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




