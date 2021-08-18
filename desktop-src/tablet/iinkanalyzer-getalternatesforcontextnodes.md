---
description: Recupera alternativas de análisis para los nodos de una colección IContextNodes especificada.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: Método IInkAnalyzer::GetAlternatesForContextNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939865"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>Método IInkAnalyzer::GetAlternatesForContextNodes

Recupera alternativas de análisis para los nodos de una colección [**IContextNodes**](icontextnodes.md) especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNodes* \[ En\]
</dt> <dd>

Colección [**IContextNodes**](icontextnodes.md) para la que se devuelven las alternativas de análisis.

</dd> <dt>

*ulMaximumAlternates* \[ En\]
</dt> <dd>

Número máximo de alternativas que se devuelven.

</dd> <dt>

*ppAlternates* \[ out\]
</dt> <dd>

El [**objeto IAnalysisAlternates**](ianalysisalternates.md) que contiene las alternativas de análisis.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAlternates* cuando ya no necesite usar el objeto .

 

El [**IAnalysisAlternate**](ianalysisalternate.md) superior se devuelve como la primera alternativa de la colección.

Los [**objetos IContextNode**](icontextnode.md) de *pContextNodes* no tienen que representar áreas adyacentes del documento.

Para cada sugerencia de análisis en nodos, [**IInkAnalyzer**](iinkanalyzer.md) devuelve solo la alternativa superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternates (Método)**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForStrokes (Método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternate (Método)**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer::ModifyTopAlternateWithConfirmation (Método)**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

