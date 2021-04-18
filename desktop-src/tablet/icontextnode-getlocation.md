---
description: Recupera la posición y el tamaño del objeto IContextNode.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'IContextNode:: GetLocation (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715229"
---
# <a name="icontextnodegetlocation-method"></a>IContextNode:: GetLocation (método)

Recupera la posición y el tamaño del objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIAnalysisRegion* \[ enuncia\]
</dt> <dd>

Puntero a la posición y tamaño del objeto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppIAnalysisRegion* cuando ya no necesite usar la región de análisis.

 

La ubicación de un nodo contenedor se determina mediante la búsqueda de la Unión de todas las ubicaciones de la hoja. La ubicación de un nodo de hoja de tinta se determina mediante la búsqueda de la Unión del rectángulo de selección de los trazos asociados. La ubicación de un nodo de hoja que no es de tinta se establece cuando se crea el nodo y se puede actualizar mediante [**IContextNode:: SetLocation**](icontextnode-setlocation.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un método auxiliar que recupera información sobre un nodo especificado, su parámetro *pContextNode* . Este método auxiliar devuelve información de los siguientes métodos.

-   [**IContextNode:: GetId**](icontextnode-getid.md)
-   [**IContextNode:: GetType**](icontextnode-gettype.md)
-   **IContextNode:: GetLocation**
-   [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode:: SetLocation**](icontextnode-setlocation.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

