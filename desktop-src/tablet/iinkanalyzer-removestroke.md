---
description: Quita el trazo especificado de IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'IInkAnalyzer:: RemoveStroke (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542006"
---
# <a name="iinkanalyzerremovestroke-method"></a>IInkAnalyzer:: RemoveStroke (método)

Quita el trazo especificado de [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Este método quita del [**IInkAnalyzer**](iinkanalyzer.md)los datos del paquete y las referencias a, el trazo especificado.

Este método quita el trazo del nodo de contexto hoja que hace referencia al trazo. Si [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina los objetos **IContextNode** y **IContextNode** antecesor que ya no tienen ningún nodo secundario.

Después de que este método quita el trazo del [**IContextNode**](icontextnode.md), actualiza la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el rectángulo de selección del trazo que se ha quitado.

Si *plStrokeId* no identifica un trazo asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar el analizador de tinta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: AddStroke (método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokeForLanguage (método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokesForLanguage (método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStrokes (método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




