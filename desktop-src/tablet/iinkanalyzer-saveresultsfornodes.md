---
description: Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: Método IInkAnalyzer::SaveResultsForNodes (IACom.h)
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
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091575"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>IInkAnalyzer::SaveResultsForNodes (método)

Guarda los resultados del análisis de una colección de nodos de contexto específica asociada a [**un IInkAnalyzer**](iinkanalyzer.md).

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

*pContextNodes* \[ En\]
</dt> <dd>

Colección [**IContextNode**](icontextnode.md) para la que se guardarán los resultados del análisis.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Número de bytes de *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ out\]
</dt> <dd>

Puntero a los datos de análisis serializados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda los resultados de análisis actuales para los objetos [**IContextNode**](icontextnode.md) en *pContextNodes* y todos sus nodos de contexto antecesores y descendientes. Este método no guarda ningún dato de trazo. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persisten.

Si el [**objeto IContextNode**](icontextnode.md) que se va a guardar solo se rellena parcialmente, este método devuelve un código de error (vea [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::LoadResults (Método)**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResults (Método)**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForStrokes (Método)**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

