---
description: Quita los trazos especificados de IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: Método IInkAnalyzer::RemoveStrokes (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574485"
---
# <a name="iinkanalyzerremovestrokes-method"></a>IInkAnalyzer::RemoveStrokes (método)

Quita los trazos especificados de [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ En\]
</dt> <dd>

Identificadores de los trazos que se quitarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Este método quita de [**IInkAnalyzer**](iinkanalyzer.md)los datos de paquetes para y las referencias a los trazos especificados.

Este método quita los trazos del nodo de contexto hoja que hace referencia a los trazos. Si algún [**IContextNode**](icontextnode.md) ya no hace referencia a ningún trazo, este método elimina el **IContextNode** y cualquier objeto **IContextNode** antecesor que ya no tenga ningún nodo secundario.

Después de que este método quita los trazos de [**IContextNode**](icontextnode.md), actualiza la región desusada del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) para incluir el cuadro de límite de los trazos quitados.

Si un trazo identificado en *plStrokes* no está asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método omite el identificador.

Si ninguno de los trazos identificados en *plStrokes* está asociado al analizador de entrada de lápiz, este método devuelve sin actualizar [**IInkAnalyzer**](iinkanalyzer.md).

Este método devuelve y el código de error cuando *plStrokes* es NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

[**IInkAnalyzer::RemoveStroke (Método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion (Método)**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




