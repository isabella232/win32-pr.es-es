---
description: Especifica la dirección de un objeto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumeración ContextLinkDirection (IACom. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910446"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="cc6b9-103">Enumeración ContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="cc6b9-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="cc6b9-104">Especifica la dirección de un objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="cc6b9-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc6b9-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="cc6b9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cc6b9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cc6b9-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ LinksWith**</span><span class="sxs-lookup"><span data-stu-id="cc6b9-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="cc6b9-108">[**IContextNode**](icontextnode.md) es un dibujo direccional que apunta fuera del [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="cc6b9-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc6b9-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ LinksFrom**</span><span class="sxs-lookup"><span data-stu-id="cc6b9-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="cc6b9-110">[**IContextNode**](icontextnode.md) es un dibujo direccional que apunta a [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="cc6b9-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc6b9-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**Vínculos de ContextLinkDirection \_**</span><span class="sxs-lookup"><span data-stu-id="cc6b9-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="cc6b9-112">No hay dibujos direccionales en el vínculo.</span><span class="sxs-lookup"><span data-stu-id="cc6b9-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="cc6b9-113">Por ejemplo, un dibujo de tinta puede subrayar una palabra de tinta.</span><span class="sxs-lookup"><span data-stu-id="cc6b9-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="cc6b9-114">No hay ninguna dirección que se infiera del subrayado.</span><span class="sxs-lookup"><span data-stu-id="cc6b9-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cc6b9-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc6b9-115">Examples</span></span>

<span data-ttu-id="cc6b9-116">En el ejemplo siguiente se toma un objeto [**IContextNode**](icontextnode.md) , `m_pSelectedNode` , y se guardan todos los objetos **IContextNode** a los que se vincula; para ello, se recorre el árbol antecesor y se agregan los objetos a un `CArray` objeto `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="cc6b9-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="cc6b9-117">`CheckHResult` es una función que toma un `HRESULT` y una cadena, y produce una excepción creada con la cadena si el `HRESULT` no es **correcto**.</span><span class="sxs-lookup"><span data-stu-id="cc6b9-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cc6b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc6b9-118">Requirements</span></span>



| <span data-ttu-id="cc6b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6b9-119">Requirement</span></span> | <span data-ttu-id="cc6b9-120">Value</span><span class="sxs-lookup"><span data-stu-id="cc6b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6b9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6b9-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cc6b9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc6b9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6b9-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc6b9-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cc6b9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc6b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc6b9-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cc6b9-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6b9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc6b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6b9-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="cc6b9-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="cc6b9-129">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="cc6b9-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




