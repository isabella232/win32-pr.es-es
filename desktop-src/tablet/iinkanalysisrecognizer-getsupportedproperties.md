---
description: Recupera los identificadores únicos globales (GUID) de las propiedades que este IInkAnalysisRecognizer puede generar para los resultados del análisis.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer:: GetSupportedProperties (método) (IACom. h)'
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
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001186"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>IInkAnalysisRecognizer:: GetSupportedProperties (método)

Recupera los identificadores únicos globales (GUID) de las propiedades que este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.

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

Número de GUID de *ppProperties*.

</dd> <dt>

*ppProperties* \[ enuncia\]
</dt> <dd>

Puntero a los GUID de las propiedades que este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppProperties* cuando ya no necesite la información.

 

Un reconocedor puede admitir las métricas de línea, los números de línea, los niveles de confianza, etc. Para obtener una lista completa de las propiedades que puede admitir un reconocedor, vea [constantes RecognitionProperty](recognitionproperty-constants.md).

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
</dt> <dt>

[Constantes de RecognitionProperty](recognitionproperty-constants.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

