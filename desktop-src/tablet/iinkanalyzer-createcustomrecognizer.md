---
description: Crea un nuevo nodo de reconocedor personalizado para el IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer:: CreateCustomRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275471"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>IInkAnalyzer:: CreateCustomRecognizer (método)

Crea un nuevo nodo de reconocedor personalizado para el [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalysisRecognizerId* \[ de\]
</dt> <dd>

Identificador único global (GUID) del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para el que se va a crear un nodo.

</dd> <dt>

*ppContextNode* \[ enuncia\]
</dt> <dd>

Un puntero al objeto [**IContextNode**](icontextnode.md) que representa el nuevo nodo de reconocedor personalizado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en ppContextNode cuando ya no necesite usar el objeto.

 

Este método crea un nuevo [**IContextNode**](icontextnode.md) con un tipo de CustomRecognizer (vea [**IContextNode:: GetType**](icontextnode-gettype.md)). A continuación, agrega el nuevo nodo de reconocedor personalizado a la colección de subnodos del nodo raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) y [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md)).

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

