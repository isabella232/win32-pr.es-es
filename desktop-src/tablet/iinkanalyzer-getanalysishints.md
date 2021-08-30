---
description: Obtiene todos los objetos IContextNode de la sugerencia de análisis que están asociados a IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: Método IInkAnalyzer::GetAnalysisHints (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b1aa2dede2e5027b3e626d3cbcc152d03348e34b87e4cbb5e9d3e2106d3b58c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008385"
---
# <a name="iinkanalyzergetanalysishints-method"></a>IInkAnalyzer::GetAnalysisHints (método)

Obtiene todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAnalysisHints* \[ out\]
</dt> <dd>

Puntero a todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis [**en IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHints* cuando ya no necesite usar el objeto .

 

Este método devuelve una colección vacía si no hay nodos de sugerencias de análisis asociados a [**IInkAnalyzer**](iinkanalyzer.md).

Un nodo de sugerencia de análisis es [**un IContextNode**](icontextnode.md) con un tipo de nodo de contexto AnalysisHint (vea [**IContextNode::GetType**](icontextnode-gettype.md) y Tipos de nodo [de contexto).](context-node-types.md)

Para agregar información de contexto a la sugerencia, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en uno de los identificadores únicos globales (GUID) en las constantes [propiedades](analysis-hint-properties.md) de sugerencias de análisis.

Para buscar qué valores de propiedad se establecen en un nodo de contexto, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md). Para buscar el valor de una propiedad, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::D eleteAnalysisHint (Método)**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHintsByName (Método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

