---
description: Recupera el objeto IAnalysisAlternate en el índice especificado de la colección.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'IAnalysisAlternates:: GetAnalysisAlternate (método) (IACom. h)'
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
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696551"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>IAnalysisAlternates:: GetAnalysisAlternate (método)

Recupera el objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulIndex* \[ de\]
</dt> <dd>

Índice de base cero del objeto [**IAnalysisAlternate**](ianalysisalternate.md) que se va a obtener.

</dd> <dt>

*ppAlternate* \[ enuncia\]
</dt> <dd>

Puntero al objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternate* cuando ya no necesite usar la alternativa de análisis.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

