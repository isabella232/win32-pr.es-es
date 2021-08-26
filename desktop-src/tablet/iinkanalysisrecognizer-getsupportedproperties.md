---
description: Recupera los identificadores únicos globales (GUID) de las propiedades que este IInkAnalysisRecognizer puede generar para los resultados del análisis.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: Método IInkAnalysisRecognizer::GetSupportedProperties (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057865"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>IInkAnalysisRecognizer::GetSupportedProperties (método)

Recupera los identificadores únicos globales (GUID) de las propiedades que [**este IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulPropertiesCount* \[ in, out\]
</dt> <dd>

Número de GUID en *ppProperties.*

</dd> <dt>

*ppProperties* \[ out\]
</dt> <dd>

Puntero a los GUID de propiedades que [**este IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) liberar la memoria de \* *ppProperties* cuando ya no necesite la información.

 

Un reconocedor puede admitir métricas de línea, números de línea, niveles de confianza, y así sucesivamente. Para obtener una lista completa de las propiedades que un reconocedor puede admitir, vea [RecognitionProperty Constants](recognitionproperty-constants.md).

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

[Constantes recognitionProperty](recognitionproperty-constants.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

