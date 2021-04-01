---
description: Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interfaz IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082153"
---
# <a name="icontextnode-interface"></a>Interfaz IContextNode

Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.

## <a name="members"></a>Miembros

La interfaz **IContextNode** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNode** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IContextNode** tiene estos métodos.



| Método                                                                                  | Descripción                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddContextLink**](icontextnode-addcontextlink.md)                                   | Agrega un nuevo [**IContextLink**](icontextlink.md) a la colección de vínculos de contexto del objeto **IContextNode** .<br/>                                                                                                          |
| [**AddPropertyData**](icontextnode-addpropertydata.md)                                 | Agrega una parte de los datos específicos de la aplicación.<br/>                                                                                                                                                                         |
| [**Confirm**](icontextnode-confirm.md)                                                 | Modifica el tipo de confirmación, que controla lo que el objeto [**IInkAnalyzer**](iinkanalyzer.md) puede cambiar sobre **IContextNode**.<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | Determina si el objeto **IContextNode** contiene datos almacenados en el identificador especificado.<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | Crea un objeto **IContextNode** secundario que solo contiene información sobre el tipo, el identificador y la ubicación.<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | Crea un nuevo objeto **IContextNode** secundario.<br/>                                                                                                                                                                       |
| [**DeleteContextLink**](icontextnode-deletecontextlink.md)                             | Elimina un objeto [**IContextLink**](icontextlink.md) de la colección de vínculos del objeto **IContextNode** .<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | Quita un **IContextNode** secundario.<br/>                                                                                                                                                                                  |
| [**GetContextLinks**](icontextnode-getcontextlinks.md)                                 | Recupera una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos **IContextNode** .<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | Recupera el identificador del objeto **IContextNode** .<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | Recupera la posición y el tamaño del objeto **IContextNode** .<br/>                                                                                                                                                    |
| [**GetParentNode**](icontextnode-getparentnode.md)                                     | Recupera el nodo primario de este **IContextNode** en el árbol de nodos de contexto.<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | Recupera el valor que indica si un objeto **IContextNode** se rellena parcialmente o está totalmente rellenado.<br/>                                                                                                   |
| [**GetPropertyData**](icontextnode-getpropertydata.md)                                 | Recupera datos específicos de la aplicación u otros datos de propiedad dado el identificador especificado.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Recupera los identificadores para los que hay datos de propiedad.<br/>                                                                                                                                                        |
| [**GetStrokeCount**](icontextnode-getstrokecount.md)                                   | Recupera el número de trazos asociados al objeto **IContextNode** .<br/>                                                                                                                                       |
| [**GetStrokeId**](icontextnode-getstrokeid.md)                                         | Recupera el identificador de trazo para el trazo al que hace referencia un valor de índice dentro del objeto **IContextNode** .<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Recupera una matriz de identificadores para los trazos dentro del objeto **IContextNode** .<br/>                                                                                                                              |
| [**GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.<br/>                                                                                                                                   |
| [**GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | Recupera los nodos secundarios directos del objeto **IContextNode** .<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | Recupera el tipo del objeto **IContextNode** .<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | Recupera un nombre de tipo legible de este **IContextNode**.<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | Recupera un valor que indica si se confirma el objeto **IContextNode** . [**IInkAnalyzer**](iinkanalyzer.md) no puede cambiar el tipo de nodo ni los trazos asociados de los objetos **IContextNode** confirmados.<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | Reordena un objeto **IContextNode** secundario especificado al índice especificado.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Quita una parte de los datos específicos de la aplicación.<br/>                                                                                                                                                                      |
| [**Reparent**](icontextnode-reparent.md)                                               | Mueve este objeto **IContextNode** de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.<br/>                                                                         |
| [**ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | Mueve los datos de trazo desde este **IContextNode** al **IContextNode** especificado.<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este **IContextNode**.<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Actualiza la posición y el tamaño de este **IContextNode**.<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | Modifica el valor que indica si este **IContextNode** se rellena parcial o totalmente.<br/>                                                                                                                   |
| [**SetStrokes**](icontextnode-setstrokes.md)                                           | Asocia los trazos especificados a este **IContextNode**.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Los tipos de nodos se describen en las constantes de [tipos de nodo de contexto](context-node-types.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un método que examina un **IContextNode**; el método hace lo siguiente:

-   Obtiene el tipo del nodo de contexto. Si el nodo de contexto es una tinta sin clasificar, una sugerencia de análisis o un nodo de reconocedor personalizado, llama a un método auxiliar para examinar propiedades específicas del tipo de nodo.
-   Si el nodo tiene subnodos, examina cada subnodo llamando a sí mismo.
-   Si el nodo es un nodo de hoja de tinta, examina los datos de trazo del nodo llamando a un método auxiliar.

Propio InkAnalysis API le permite crear un nodo de línea que contiene palabras de tinta y palabras de texto. Sin embargo, el analizador pasará por alto estos nodos mixtos y los tratará como nodos externos. Esto afectará a la precisión de análisis de la detección de anotaciones manuscritas cuando el usuario final escribe en este nodo mixto o en torno a este.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

