---
description: Guarda todos los resultados de análisis de un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer:: SaveResults (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360335"
---
# <a name="iinkanalyzersaveresults-method"></a>IInkAnalyzer:: SaveResults (método)

Guarda todos los resultados de análisis de un [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulSerializedDataSize* \[ enuncia\]
</dt> <dd>

Número de bytes de *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los resultados del análisis guardado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda todos los resultados del análisis actual, que incluyen la sugerencia de análisis actual y los nodos de reconocedor personalizados (vea [**IContextNode:: GetType**](icontextnode-gettype.md)). Este método no guarda ningún dato de trazo. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los trazos correspondientes si guarda los datos.

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

[**IInkAnalyzer:: SaveResultsForNodes (método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer:: SaveResultsForStrokes (método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

