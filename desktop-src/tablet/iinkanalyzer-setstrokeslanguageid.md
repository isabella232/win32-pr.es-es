---
description: Cambia el identificador de configuración regional para los trazos especificados.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'IInkAnalyzer:: SetStrokesLanguageId (método) (IACom. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705694"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>IInkAnalyzer:: SetStrokesLanguageId (método)

Cambia el identificador de configuración regional para los trazos especificados.

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

*ulStrokeIdCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en *plStrokes*.

</dd> <dt>

*plStrokes* \[ de\]
</dt> <dd>

Matriz de identificadores para los trazos a los que se va a asignar el identificador de configuración regional.

</dd> <dt>

*lStrokesLCID* \[ de\]
</dt> <dd>

Identificador de configuración regional que se va a asignar a los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

La configuración regional de un trazo se establece al agregar el trazo mediante una llamada al método [**IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md), el método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)o [**IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para obtener la configuración regional asignada actualmente a un trazo, llame al [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Los trazos especificados se mueven a un nodo de tinta sin clasificar (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) que contiene los trazos del mismo idioma. Si no existe tal [**IContextNode**](icontextnode.md) , este método crea un nuevo nodo de tinta sin clasificar y le mueve los trazos. Un nodo de tinta sin clasificar es un **IContextNode** que tiene un tipo de UnclassifiedInk.

Si este método mueve trazos de un [**IContextNode**](icontextnode.md) que no es un nodo de tinta sin clasificar, este método también agrega los cuadros de límite de los trazos a la región desfasada del analizador de tinta (vea el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Este método no mueve un trazo si el parámetro *lStrokeLCID* coincide con el identificador de idioma actual del trazo.

Si un trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.

Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

Este método devuelve un código de error cuando strokeIds es **null**.

Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**IInkAnalyzer:: GetStrokeLanguageId (método)**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**IInkAnalyzer:: SetStrokeLanguageId (método)**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

