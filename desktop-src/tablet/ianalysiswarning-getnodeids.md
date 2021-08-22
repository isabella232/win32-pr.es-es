---
description: Devuelve los identificadores de los nodos de contexto pertinentes asociados a esta advertencia.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: Método IAnalysisWarning::GetNodeIds (IACom.h)
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
ms.openlocfilehash: 97e6f4fde66faef14402c815f6b95517a2bd19adfb90eac4e865383770bc753f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967484"
---
# <a name="ianalysiswarninggetnodeids-method"></a>IAnalysisWarning::GetNodeIds (método)

Devuelve los identificadores de los nodos de contexto pertinentes asociados a esta advertencia.

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

Número de identificadores únicos globales (GUID) en *ppNodeIds.*

</dd> <dt>

*ppNodeIds* \[ out\]
</dt> <dd>

Puntero a una matriz de GUID que identifica los nodos de contexto asociados a esta advertencia de análisis, o **NULL** si no hay nodos de contexto asociados a la advertencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si *ppNodeIds se* pasa como **NULL,** el **método GetNodeIds** devuelve **S \_ OK** y el número de rectángulos se devuelve en *pulCount*.

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppNodeIds* cuando ya no necesite la información.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo obtener los objetos [**IContextNode**](icontextnode.md) que están en [**IAnalysisWarning**](ianalysiswarning.md), y cómo obtener solo el número de objetos `warning` **IContextNode.**


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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::FindNode (Método)**](iinkanalyzer-findnode.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

