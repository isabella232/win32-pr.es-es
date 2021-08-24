---
description: Obtiene el IContextNode raíz del árbol de contexto del objeto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: Método IInkAnalyzer::GetRootNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713425"
---
# <a name="iinkanalyzergetrootnode-method"></a>IInkAnalyzer::GetRootNode (método)

Obtiene el [**IContextNode raíz**](icontextnode.md) del árbol de contexto del objeto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppRootNode* \[ out\]
</dt> <dd>

[**IContextNode raíz**](icontextnode.md) del árbol de contexto del objeto [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppRootNode* cuando ya no necesite usar el nodo raíz.

 

[**IInkAnalyzer**](iinkanalyzer.md) mantiene un árbol de [**objetos IContextNode.**](icontextnode.md) Estos objetos contienen entradas para el análisis y los resultados del análisis. Cuando los trazos se agregan inicialmente a **IInkAnalyzer,** **IInkAnalyzer** los asigna a un **IContextNode** de tipo UnclassifiedInk (vea [**IContextNode::GetType**](icontextnode-gettype.md) y Tipos de nodo de [contexto).](context-node-types.md) Después de analizar los trazos, **IInkAnalyzer** los asigna a los objetos **IContextNode** adecuados del árbol. Para obtener más información sobre el uso de **IInkAnalyzer para** analizar la entrada de lápiz, vea [Ink Analysis Overview](ink-analysis-overview.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un método que recorre el árbol de resultados [**de IContextNode**](icontextnode.md) del analizador de entrada manuscrita. Si IInkAnlyzer no está realizando actualmente análisis de entrada de lápiz, el método hace lo siguiente.

-   Obtiene la cadena de reconocimiento superior.
-   Obtiene el nodo raíz del analizador de entrada de lápiz.
-   Llama a un método auxiliar, `ExploreContextNode` , para examinar el nodo raíz y sus nodos secundarios.


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



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

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

