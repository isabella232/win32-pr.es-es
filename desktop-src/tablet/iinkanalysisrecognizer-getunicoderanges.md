---
description: Recupera una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: Método IInkAnalysisRecognizer::GetUnicodeRanges (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cf8c0fe75d2eff0cdd8f2f9d3eb5366f6bab4dd4588c854455804ce4196971bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008405"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>IInkAnalysisRecognizer::GetUnicodeRanges (método)

Recupera una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulNumberOfRanges* \[ in, out\]
</dt> <dd>

Número de intervalos de caracteres a los que apunta *ppulLowUnicode.*

</dd> <dt>

*ppulLowUnicode* \[ out\]
</dt> <dd>

Puntero a una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.

</dd> <dt>

*ppusUnicodeRangeLength* \[ out\]
</dt> <dd>

Puntero a una matriz de valores que indica la longitud de cada matriz apunta a *mediante ppulLowUnicode*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




