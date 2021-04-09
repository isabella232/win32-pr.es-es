---
description: Obtiene todos los objetos IContextNode de la sugerencia de análisis que están asociados a IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'IInkAnalyzer:: GetAnalysisHints (método) (IACom. h)'
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
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154415"
---
# <a name="iinkanalyzergetanalysishints-method"></a>IInkAnalyzer:: GetAnalysisHints (método)

Obtiene todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAnalysisHints* \[ enuncia\]
</dt> <dd>

Un puntero a todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis en el [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHints* cuando ya no necesite usar el objeto.

 

Este método devuelve una colección vacía si no hay ningún nodo de sugerencia de análisis asociado al [**IInkAnalyzer**](iinkanalyzer.md).

Un nodo de sugerencia de análisis es un [**IContextNode**](icontextnode.md) con un tipo de nodo de contexto AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md)).

Para agregar información de contexto a la sugerencia, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en uno de los identificadores únicos globales (GUID) en las constantes de [las propiedades](analysis-hint-properties.md) de la sugerencia de análisis.

Para averiguar qué valores de propiedad se establecen en un nodo de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md). Para buscar el valor de una propiedad, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::D método eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHintsByName (método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

