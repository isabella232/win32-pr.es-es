---
description: Guarda los resultados del análisis de los trazos especificados asociados a un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: Método IInkAnalyzer::SaveResultsForStrokes (IACom.h)
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
ms.openlocfilehash: fd9a95ada1385fdbb6dbc5a1e22cde0ef319156ad7c3cd7782e911d06696af37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091573"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>IInkAnalyzer::SaveResultsForStrokes (método)

Guarda los resultados del análisis de los trazos especificados asociados a [**un IInkAnalyzer**](iinkanalyzer.md).

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

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo en **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ En\]
</dt> <dd>

Matriz de identificadores de trazo.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Número de bytes de *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Puntero a los datos de análisis serializados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) en \* *ppbSerializedData* cuando ya no necesite la información.

 

Este método guarda los resultados del análisis actuales para los trazos especificados. Este método guarda los objetos [**IContextNode**](icontextnode.md) de hoja de lápiz que contienen los trazos y todos los antecesores de esos nodos de contexto. Este método no guarda ningún nodo de sugerencia de análisis o datos de trazo. Es responsabilidad de la aplicación sincronizar los resultados del análisis y los datos de trazo correspondientes, si persisten.

Este método devuelve un código de error cuando un objeto [**IContextNode**](icontextnode.md) que se va a guardar se rellena parcialmente (vea [**IContextNode::GetPartiallyPopulated).**](icontextnode-getpartiallypopulated.md)

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

[**IInkAnalyzer::SaveResultsForNodes (Método)**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

