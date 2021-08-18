---
description: 'Método IInkAnalyzer::Search: proporciona una búsqueda aproximada basada en frases sin mayúsculas y minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: Método IInkAnalyzer::Search (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a5ebbec010d84f510d9bd2786b20fee1deaa34039720d842df77cbe0f1ca9825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091513"
---
# <a name="iinkanalyzersearch-method"></a>IInkAnalyzer::Search (método)

Proporciona una búsqueda aproximada y sin mayúsculas de minúsculas basada en frases para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
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

Frase que se encontrará en las alternativas para los trazos analizados actualmente.

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

Número de id. de trazo en *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ out\]
</dt> <dd>

Puntero a una matriz de los ID de trazo que representan un conjunto de conjuntos de trazos.

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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 




