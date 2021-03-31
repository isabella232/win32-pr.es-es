---
description: Quita los trazos especificados de IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'IInkAnalyzer:: RemoveStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154412"
---
# <a name="iinkanalyzerremovestrokes-method"></a>IInkAnalyzer:: RemoveStrokes (método)

Quita los trazos especificados de [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ de\]
</dt> <dd>

Los identificadores de los trazos que se van a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Este método quita los datos de paquete de y las referencias a los trazos especificados de [**IInkAnalyzer**](iinkanalyzer.md).

Este método quita los trazos del nodo de contexto hoja que hace referencia a los trazos. Si alguna [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina los objetos **IContextNode** y **IContextNode** antecesor que ya no tienen ningún nodo secundario.

Después de que este método quita los trazos de [**IContextNode**](icontextnode.md), actualiza la región desfasada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer:: GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el rectángulo de selección de los trazos que se han quitado.

Si un trazo identificado en *plStrokes* no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.

Si ninguno de los trazos identificados en *plStrokes* están asociados al analizador de tinta, este método devuelve sin actualizar [**IInkAnalyzer**](iinkanalyzer.md).

Este método devuelve y el código de error cuando *plStrokes* es NULL.

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

[**IInkAnalyzer:: RemoveStroke (método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer:: GetDirtyRegion (método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




