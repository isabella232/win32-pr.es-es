---
description: Recupera la región del documento correspondiente a los cambios que se realizaron en el árbol de nodos de contexto del objeto IInkAnalyzer como resultado del análisis de tinta.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus:: GetAppliedChangesRegion (método) (IACom. h)'
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
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542086"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>IAnalysisStatus:: GetAppliedChangesRegion (método)

Recupera la región del documento correspondiente a los cambios que se realizaron en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado del análisis de tinta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAppliedChangesRegion* \[ enuncia\]
</dt> <dd>

Puntero al [**IAnalysisRegion**](ianalysisregion.md) del documento en el que se realizaron los cambios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pAppliedChangesRegion* cuando ya no necesite usar la región de análisis.

 

Este método se usa con más frecuencia cuando la aplicación recibe información con fines de depuración y necesita invalidar el área en la que se pueden producir cambios para que se dibuje la información de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

