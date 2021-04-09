---
description: Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'IInkAnalyzer:: Search (método) (IACom. h)'
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
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154408"
---
# <a name="iinkanalyzersearch-method"></a>IInkAnalyzer:: Search (método)

Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.

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

*bstrPhraseToMatch* \[ de\]
</dt> <dd>

La frase que se encontrará en las alternativas para los trazos analizados actualmente.

</dd> <dt>

*pulSearchResultCount* \[ in, out\]
</dt> <dd>

Número máximo de resultados que se devuelven de la búsqueda.

</dd> <dt>

*ppulStrokeCountPerResult* \[ enuncia\]
</dt> <dd>

Puntero a una matriz del número de trazos en cada resultado de búsqueda.

</dd> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Número de identificadores de trazo en *ppulStrokeIds*.

</dd> <dt>

*ppulStrokeIds* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de identificadores de trazo que representa un conjunto de conjuntos de trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Esta búsqueda busca subcadenas con varias palabras y una sola palabra. Se busca en los resultados de reconocimiento alternativos y en los segmentaciones alternativos.

Todas las cadenas de entrada se convertirán en un único uso de mayúsculas y minúsculas para la comparación mediante el LCID del subproceso actual para realizar esta conversión para respetar las convenciones culturales de casos.

La cadena que se pasa se trata como una frase. Las palabras y los caracteres deben aparecer en el alterantes para los trazos en el orden especificado. La primera y la última palabra de la frase pueden coincidir como subcadenas (la primera palabra aparece al final de una alternativa y la última palabra aparece en el begginging de una), pero otras palabras (las que se encuentran dentro de la frase) deben aparecer como palabras completas.

Si la cadena que se pasa no tiene ningún espacio en blanco entre los caracteres, la subcadena se puede encontrar en cualquier parte dentro de una sola palabra en una alternativa.

Solo la presencia o ausencia de espacio en blanco entre los caracteres cambia los resultados de la búsqueda. Se omiten los espacios en blanco que no están rodeados por caracteres. Se omite el tipo de espacio en blanco (una tabulación o un espacio entre los caracteres darán el mismo resultado). La cantidad de espacio en blanco no importa: un espacio o dos espacios entre caracteres darán el mismo resultado.

La búsqueda no genera eventos PopulateContextNode. Solo se buscarán los trazos que ya se han rellenado.

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
</dt> </dl>

 

 




