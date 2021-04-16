---
description: Devuelve los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning:: GetNodeIds (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542078"
---
# <a name="ianalysiswarninggetnodeids-method"></a>IAnalysisWarning:: GetNodeIds (método)

Devuelve los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulCount* \[ in, out\]
</dt> <dd>

El número de identificadores únicos globales (GUID) en *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de GUID que identifica los nodos de contexto asociados a esta advertencia de análisis, o **null** si no hay ningún nodo de contexto asociado a la advertencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si *ppNodeIds* se pasa como **null**, el método **GetNodeIds** devuelve **S \_ correcto** y el número de rectángulos se devuelve en *pulCount*.

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppNodeIds* cuando ya no necesite la información.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo obtener los objetos [**IContextNode**](icontextnode.md) que se encuentran en [**IAnalysisWarning**](ianalysiswarning.md), `warning` y cómo obtener solo el número de objetos **IContextNode**


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer:: FindNode (método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

