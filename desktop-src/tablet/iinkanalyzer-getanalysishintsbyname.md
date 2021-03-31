---
description: Recupera todos los objetos IContextNode de la sugerencia de análisis que están asociados a IInkAnalyzer y que tienen el nombre especificado.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer:: GetAnalysisHintsByName (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275468"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a>IInkAnalyzer:: GetAnalysisHintsByName (método)

Recupera todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a [**IInkAnalyzer**](iinkanalyzer.md) y que tienen el nombre especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hintName* \[ de\]
</dt> <dd>

Nombre de la sugerencia que se va a buscar.

</dd> <dt>

*ppAnalysisHints* \[ enuncia\]
</dt> <dd>

La sugerencia de análisis [**IContextNode**](icontextnode.md) objetos en el [**IInkAnalyzer**](iinkanalyzer.md) que tienen el nombre especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces: Análisis de tinta](classes-and-interfaces---ink-analysis.md) de los valores devueltos.

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHints* cuando ya no necesite usar el objeto.

 

Este método devuelve una colección vacía si no hay ningún nodo de sugerencia de análisis asociado a [**IInkAnalyzer**](iinkanalyzer.md).

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

[**IInkAnalyzer:: GetAnalysisHints (método)**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

