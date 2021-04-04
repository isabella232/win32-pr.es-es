---
description: Recupera una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer:: GetUnicodeRanges (método) (IACom. h)'
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
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908019"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>IInkAnalysisRecognizer:: GetUnicodeRanges (método)

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

El número de intervalos de caracteres a los que apunta *ppulLowUnicode*.

</dd> <dt>

*ppulLowUnicode* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.

</dd> <dt>

*ppusUnicodeRangeLength* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de valores que indica la longitud de cada matriz que apunta a *ppulLowUnicode*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




