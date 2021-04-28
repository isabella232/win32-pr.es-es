---
description: 'Método IInkAnalyzer::SearchWithLanguageId: proporciona una búsqueda aproximada basada en frases sin mayúsculas y minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.'
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: Método IInkAnalyzer::SearchWithLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 201469933da10b0d68a4d3a50e63c42f8d01d2dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083663"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a>IInkAnalyzer::SearchWithLanguageId (método)

Proporciona una búsqueda aproximada basada en frases sin mayúsculas de minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPhraseToMatch* \[ En\]
</dt> <dd>

Frase que se encontrará en las alternativas de los trazos analizados actualmente.

</dd> <dt>

*lSearchStringLanguageId* \[ En\]
</dt> <dd>

LCID asociado a la cadena que se pasa. Se usa para convertir el caso internamente para admitir comparaciones que no tienen en cuenta mayúsculas de minúsculas.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

Número máximo de resultados devueltos por la búsqueda.

</dd> <dt>

*ppulStrokeCountPerResult* \[ out\]
</dt> <dd>

Puntero a una matriz del número de trazos en cada resultado de búsqueda.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Número de id. de trazo en *ppulStrokeIds.*

</dd> <dt>

*ppulStrokeIds* \[ out\]
</dt> <dd>

Puntero a una matriz de los IDs de trazo que representan un conjunto de conjuntos de trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Esta búsqueda busca subcadenas de varias palabras y palabras únicas. Se buscan resultados de reconocimiento alternativos y segmentaciones alternativas.

Todas las cadenas entrantes se convertirán en un solo uso de mayúsculas y minúsculas para la comparación mediante el LCID del subproceso actual para realizar esta conversión con el fin de respetar las convenciones de casos culturales.

La cadena pasada se trata como una frase. Las palabras y los caracteres deben aparecer en los alteradores de los trazos en el orden especificado. La primera y la última palabra de la frase pueden coincidir como subcadenas (la primera palabra que aparece al final de una alternativa y la última palabra que aparece al mezquite de una), pero cualquier otra palabra (las que están dentro de la frase) debe aparecer como palabras enteras.

Si la cadena pasada no tiene ningún espacio en blanco entre caracteres, la subcadena se puede encontrar en cualquier lugar dentro de una sola palabra en una alternativa.

Solo la presencia o ausencia de espacios en blanco entre caracteres cambia los resultados de la búsqueda. Se omite el espacio en blanco que no está rodeado por caracteres. Se omite el tipo de espacio en blanco (una pestaña o un espacio entre caracteres dará el mismo resultado). La cantidad de espacios en blanco no importa: un espacio o dos espacios entre caracteres darán el mismo resultado.

La búsqueda no genera eventos PopulateContextNode. Solo se buscarán los trazos que ya se han rellenado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




