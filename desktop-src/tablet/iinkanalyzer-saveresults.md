---
description: Guarda todos los resultados del análisis de un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: Método IInkAnalyzer::SaveResults (IACom.h)
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
ms.openlocfilehash: 216f238776cf88a24d10f57671aa4f03c71d07962ff480d5b219653a5c9d338e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091995"
---
# <a name="iinkanalyzersaveresults-method"></a>IInkAnalyzer::SaveResults (método)

Guarda todos los resultados del análisis de [**un IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulSerializedDataSize* \[ out\]
</dt> <dd>

Número de bytes de *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ out\]
</dt> <dd>

Matriz que contiene los resultados del análisis guardados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda todos los resultados de análisis actuales, que incluyen la sugerencia de análisis actual y los nodos de reconocedor personalizados (vea [**IContextNode::GetType**](icontextnode-gettype.md)). Este método no guarda ningún dato de trazo. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los trazos correspondientes si conserva los datos.

Este método devuelve un código de error cuando un objeto [**IContextNode**](icontextnode.md) que se va a guardar se rellena parcialmente (vea [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

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
</dt> <dt>

[**IInkAnalyzer::LoadResults (Método)**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForNodes (Método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForStrokes (Método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

