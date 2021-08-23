---
description: Recupera el identificador único global (GUID) del reconocedor.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: Método IInkAnalysisRecognizer::GetGuid (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b5fbf2b07b2a63f2fdb088c38a5e03e4182c4e38528208c039f927b282755344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596745"
---
# <a name="iinkanalysisrecognizergetguid-method"></a>IInkAnalysisRecognizer::GetGuid (método)

Recupera el identificador único global (GUID) del reconocedor.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ out\]
</dt> <dd>

GUID que identifica este [**objeto IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

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
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




