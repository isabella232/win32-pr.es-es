---
description: Obtiene el número de trazos asociados al objeto IContextNode.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: Método IContextNode::GetStrokeCount (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572424"
---
# <a name="icontextnodegetstrokecount-method"></a>IContextNode::GetStrokeCount (método)

Obtiene el número de trazos asociados al [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulStrokeCount* \[ out\]
</dt> <dd>

Número de trazos asociados al [**objeto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Solo los nodos de contexto de hoja de lápiz tienen datos de trazo asociados (vea [**IContextNode::GetType).**](icontextnode-gettype.md)

## <a name="examples"></a>Ejemplos

En este ejemplo se muestra un método, `ExploreContextNode` , que examina un [**IContextNode**](icontextnode.md). El método hace lo siguiente:

-   Obtiene el tipo del nodo de contexto.
-   Examina propiedades específicas del tipo de nodo llamando a un método auxiliar, si el nodo de contexto es un nodo de lápiz, sugerencia de análisis o reconocedor personalizado sin clasificar.
-   Examina cada subnodo mediante una llamada a sí mismo, si el nodo tiene subnodos.
-   Examina los datos de trazo del nodo llamando a un método auxiliar, si el nodo es un nodo hoja de entrada de lápiz.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**IContextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




