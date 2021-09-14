---
description: Recupera la cadena de mejor resultado de la operación de reconocimiento para todo el árbol de nodos de contexto en IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: Método IInkAnalyzer::GetRecognizedString (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360002"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>IInkAnalyzer::GetRecognizedString (método)

Recupera la cadena de mejor resultado de la operación de reconocimiento para todo el árbol de nodos de contexto en [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Cadena de mejor resultado de la operación de reconocimiento para todo el árbol de nodos de contexto en [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para *pbstrRecognizedString* cuando ya no necesite usar la cadena.

 

Este método devuelve el mismo valor que los datos de propiedad del nodo raíz para la cadena reconocida. (Vea [**IInkAnalyzer::GetRootNode (Método),**](iinkanalyzer-getrootnode.md) [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)y [Propiedades del nodo de contexto).](context-node-properties.md)

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

