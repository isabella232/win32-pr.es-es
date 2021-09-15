---
description: Cambia el identificador de configuración regional de los trazos especificados.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: Método IInkAnalyzer::SetStrokesLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360297"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>IInkAnalyzer::SetStrokesLanguageId (método)

Cambia el identificador de configuración regional de los trazos especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
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

Matriz de identificadores para los trazos a los que se va a asignar el identificador de configuración regional.

</dd> <dt>

*lStrokesLCID* \[ En\]
</dt> <dd>

Identificador de configuración regional que se asignará a los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

La configuración regional de un trazo se establece al agregar el trazo llamando al método [**IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage ( Método**](iinkanalyzer-addstrokeforlanguage.md)), [**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer::AddStrokesForLanguage (Método**](iinkanalyzer-addstrokesforlanguage.md)). Para obtener la configuración regional asignada actualmente a un trazo, llame al método [**IInkAnalyzer::GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Los trazos especificados se mueven a un nodo de entrada de lápiz sin clasificar (vea [**IContextNode::GetType**](icontextnode-gettype.md)) que contiene trazos del mismo lenguaje. Si no existe [**este IContextNode,**](icontextnode.md) este método crea un nuevo nodo de entrada de lápiz sin clasificar y mueve los trazos a él. Un nodo de entrada de lápiz sin clasificar es **un IContextNode** que tiene un tipo UnclassifiedInk.

Si este método mueve trazos de un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar, este método también agrega los rectángulos delimitadores de los trazos a la región desusada del analizador de entrada de lápiz (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el *parámetro lStrokeLCID* coincide con el identificador de idioma actual del trazo.

Si un trazo especificado no está asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método omite el identificador.

Si ninguno de los trazos especificados identifica un trazo asociado a [**IInkAnalyzer,**](iinkanalyzer.md)este método devuelve sin actualizar **IInkAnalyzer**.

Este método devuelve un código de error cuando strokeIds es **NULL.**

Para obtener más información sobre los identificadores de idioma, vea [Constantes y cadenas de identificador de idioma.](/windows/desktop/Intl/language-identifier-constants-and-strings)

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

[**IInkAnalyzer::GetStrokeLanguageId (Método)**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokeLanguageId (Método)**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

