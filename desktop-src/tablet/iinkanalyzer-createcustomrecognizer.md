---
description: Crea un nuevo nodo de reconocedor personalizado para IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: Método IInkAnalyzer::CreateCustomRecognizer (IACom.h)
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
ms.openlocfilehash: d30a829107710e1349917ced0a9068108bccd4c120faf3aa96ceed375c350449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043962"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>Método IInkAnalyzer::CreateCustomRecognizer

Crea un nuevo nodo de reconocedor personalizado para [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInkAnalysisRecognizerId* \[ En\]
</dt> <dd>

Identificador único global (GUID) del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para el que se va a crear un nodo.

</dd> <dt>

*ppContextNode* \[ out\]
</dt> <dd>

Puntero al objeto [**IContextNode**](icontextnode.md) que representa el nuevo nodo de reconocedor personalizado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en ppContextNode cuando ya no necesite usar el objeto .

 

Este método crea un [**nuevo IContextNode con**](icontextnode.md) un tipo de CustomRecognizer (vea [**IContextNode::GetType).**](icontextnode-gettype.md) A continuación, agrega el nuevo nodo de reconocedor personalizado a la colección de subnodos del nodo raíz del objeto [**IInkAnalyzer**](iinkanalyzer.md) (vea [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer::GetRootNode (Método).**](iinkanalyzer-getrootnode.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::GetInkAnalysisRecognizersByPriority (Método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

