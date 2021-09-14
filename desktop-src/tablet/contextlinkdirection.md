---
description: Especifica la dirección de un objeto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumeración ContextLinkDirection (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256814"
---
# <a name="contextlinkdirection-enumeration"></a>Enumeración ContextLinkDirection

Especifica la dirección de un [**objeto IContextLink.**](icontextlink.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ LinksWith**
</dt> <dd>

[**IContextNode es**](icontextnode.md) un dibujo direccional que apunta lejos de [**IContextLink.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ LinksFrom**
</dt> <dd>

[**IContextNode es**](icontextnode.md) un dibujo direccional que apunta a [**IContextLink.**](icontextlink.md)

</dd> <dt>

<span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection \_ LinksTo**
</dt> <dd>

No hay ningún dibujo direccional en el vínculo. Por ejemplo, un dibujo con lápiz puede subraya una palabra de lápiz. No hay ninguna dirección deducida del subrayado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se toma un objeto [**IContextNode,**](icontextnode.md) , y se guarda todos los objetos `m_pSelectedNode` **IContextNode** a los que se vincula recorrindo el árbol antecesor y agregando los objetos a un `CArray` objeto , `linkedToNodes` . `CheckHResult` es una función que toma y una cadena, y produce una excepción creada con la `HRESULT` cadena si no es `HRESULT` **SUCCESS**.


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




