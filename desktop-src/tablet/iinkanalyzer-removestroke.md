---
description: Quita el trazo especificado del IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: Método IInkAnalyzer::RemoveStroke (IACom.h)
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
ms.openlocfilehash: dd0a972ed776c40fc42d695df2058c62f9af84f8fc09155758d197772e9abfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092015"
---
# <a name="iinkanalyzerremovestroke-method"></a>IInkAnalyzer::RemoveStroke (método)

Quita el trazo especificado de [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Este método quita los datos de paquetes para el trazo especificado de [**IInkAnalyzer**](iinkanalyzer.md)y las referencias a .

Este método quita el trazo del nodo de contexto hoja que hace referencia al trazo. Si [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina el **IContextNode** y cualquier objeto **IContextNode** antecesor que ya no tenga nodos secundarios.

Después de que este método quite el trazo del [**IContextNode**](icontextnode.md), actualiza la región desusada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el rectángulo delimitador del trazo quitado.

Si *plStrokeId* no identifica un trazo asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método devuelve sin actualizar el analizador de entrada de lápiz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::AddStroke (Método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage (Método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage (Método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes (Método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion (Método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




