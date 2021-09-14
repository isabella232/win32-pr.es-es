---
description: Cambia el identificador de configuración regional del trazo especificado.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: Método IInkAnalyzer::SetStrokeLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256731"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>IInkAnalyzer::SetStrokeLanguageId (método)

Cambia el identificador de configuración regional del trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo al que se va a asignar el identificador de configuración regional.

</dd> <dt>

*lStrokeLCID* \[ En\]
</dt> <dd>

Identificador de configuración regional que se asignará al trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

La configuración regional de un trazo se establece al agregar el trazo llamando al método [**IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage ( Método**](iinkanalyzer-addstrokeforlanguage.md)), [**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer::AddStrokesForLanguage (Método**](iinkanalyzer-addstrokesforlanguage.md)). Para obtener la configuración regional asignada actualmente a un trazo, llame al método [**IInkAnalyzer::GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

El trazo especificado se mueve a un nodo de entrada de lápiz sin clasificar (vea [**IContextNode::GetType**](icontextnode-gettype.md)) que contiene trazos del mismo lenguaje. Si no existe [**este IContextNode,**](icontextnode.md) este método crea un nuevo nodo de entrada de lápiz sin clasificar y mueve el trazo a él. Un nodo de entrada de lápiz sin clasificar es **un IContextNode** que tiene un tipo UnclassifiedInk.

Si este método mueve un trazo desde un [**IContextNode**](icontextnode.md) que no es un nodo de entrada de lápiz sin clasificar, este método también agrega el rectángulo delimitador del trazo a la región desusada del analizador de entrada de lápiz (vea [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el *parámetro lStrokeLCID* coincide con el identificador de idioma actual del trazo.

Si el trazo especificado no está asociado a [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

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

[**IInkAnalyzer::SetStrokesLanguageId (Método)**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

