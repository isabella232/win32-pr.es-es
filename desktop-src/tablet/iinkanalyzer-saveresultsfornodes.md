---
description: Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer:: SaveResultsForNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154409"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>IInkAnalyzer:: SaveResultsForNodes (método)

Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNodes* \[ de\]
</dt> <dd>

Colección de [**IContextNode**](icontextnode.md) para la que se van a guardar los resultados del análisis.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Número de bytes de *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ enuncia\]
</dt> <dd>

Puntero a los datos de análisis serializados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda los resultados de análisis actuales de los objetos [**IContextNode**](icontextnode.md) de *pContextNodes* y de todos sus nodos de contexto antecesores y descendientes. Este método no guarda ningún dato de trazo. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persiste.

Si el objeto [**IContextNode**](icontextnode.md) que se va a guardar solo se rellena parcialmente, este método devuelve un código de error (vea [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**IInkAnalyzer:: SaveResultsForStrokes (método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

