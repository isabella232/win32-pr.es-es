---
description: Recupera los identificadores de las configuraciones regionales que admite IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: Método IInkAnalysisRecognizer::GetLanguages (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a94b85dfe9a6b5dbbd755ff1e0a4cf2d68dccd5178da6d0578d6f50e8b48936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350975"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>IInkAnalysisRecognizer::GetLanguages (método)

Recupera los identificadores de las configuraciones regionales que [**admite IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulLanguagesCount* \[ in, out\]
</dt> <dd>

Número de identificadores en *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ out\]
</dt> <dd>

Puntero a los identificadores de las configuraciones regionales que [**admite este IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppulLanguages* cuando ya no necesite la información.

 

Este método devuelve una matriz vacía para reconocedores de objetos y gestos.

Para obtener más información sobre los identificadores de idioma, vea [Constantes y cadenas de identificador de idioma.](/windows/desktop/Intl/language-identifier-constants-and-strings)

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
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

