---
description: Guarda los resultados del análisis para los trazos especificados asociados a un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer:: SaveResultsForStrokes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360334"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>IInkAnalyzer:: SaveResultsForStrokes (método)

Guarda los resultados del análisis para los trazos especificados asociados a un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ de\]
</dt> <dd>

Matriz de identificadores de trazo.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Número de bytes de *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Puntero a los datos de análisis serializados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda los resultados del análisis actual para los trazos especificados. Este método guarda los objetos [**IContextNode**](icontextnode.md) de hoja de tinta que contienen los trazos y todos los antecesores de esos nodos de contexto. Este método no guarda ningún nodo de datos de trazo o de sugerencia de análisis. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persiste.

Este método devuelve un código de error cuando se rellena parcialmente un objeto [**IContextNode**](icontextnode.md) que se va a guardar (vea [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**IInkAnalyzer:: LoadResults (método)**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResults (método)**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResultsForNodes (método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

