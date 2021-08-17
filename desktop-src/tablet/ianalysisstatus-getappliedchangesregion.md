---
description: Recupera la región del documento que corresponde a los cambios realizados en el árbol de nodos de contexto del objeto IInkAnalyzer como resultado del análisis de entrada de lápiz.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: Método IAnalysisStatus::GetAppliedChangesRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044998"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>IAnalysisStatus::GetAppliedChangesRegion (método)

Recupera la región del documento que corresponde a los cambios realizados en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado del análisis de entrada de lápiz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAppliedChangesRegion* \[ out\]
</dt> <dd>

Puntero a [**IAnalysisRegion**](ianalysisregion.md) del documento donde se realizaron los cambios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pAppliedChangesRegion* cuando ya no necesite usar la región de análisis.

 

Este método se usa con más frecuencia cuando la aplicación recibe información con fines de depuración y necesita invalidar el área donde pueden producirse cambios para que se pinte la información de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

