---
description: Obtiene el valor de cadena reconocido del objeto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: Método IAnalysisAlternate::GetRecognizedString (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256784"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>IAnalysisAlternate::GetRecognizedString (método)

Obtiene el valor de cadena reconocido del [**objeto IAnalysisAlternate.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Puntero al **BSTR** que se establece en el valor de cadena reconocido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer::GetRecognizedString (Método)**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




