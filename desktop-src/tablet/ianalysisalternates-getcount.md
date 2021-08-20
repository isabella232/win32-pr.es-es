---
description: Recupera el número de objetos IAnalysisAlternate contenidos en la colección IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: Método IAnalysisAlternates::GetCount (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967494"
---
# <a name="ianalysisalternatesgetcount-method"></a>IAnalysisAlternates::GetCount (método)

Recupera el número de [**objetos IAnalysisAlternate**](ianalysisalternate.md) contenidos en la [**colección IAnalysisAlternates.**](ianalysisalternates.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Entero de 32 bits sin signo que se establece en el número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contenidos en la [**colección IAnalysisAlternates.**](ianalysisalternates.md)

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




