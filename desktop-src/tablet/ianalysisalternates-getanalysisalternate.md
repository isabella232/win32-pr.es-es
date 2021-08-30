---
description: Recupera el objeto IAnalysisAlternate en el índice especificado dentro de la colección.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: Método IAnalysisAlternates::GetAnalysisAlternate (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ab0ccc52bcb390e27f78dd14ec19857c2065b92f7b1b0eb67a34fedf952f4e94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940661"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>IAnalysisAlternates::GetAnalysisAlternate (método)

Recupera el [**objeto IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado dentro de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulIndex* \[ En\]
</dt> <dd>

Índice de base cero del objeto [**IAnalysisAlternate**](ianalysisalternate.md) que se obtiene.

</dd> <dt>

*ppAlternate* \[ out\]
</dt> <dd>

Puntero al objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado dentro de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternate* cuando ya no necesite usar la alternativa de análisis.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

