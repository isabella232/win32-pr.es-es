---
title: Tipo complejo de XmlType
description: Define un fragmento XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- XmlType tipo complejo EventLog
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422294"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="99ffe-104">Tipo complejo de XmlType</span><span class="sxs-lookup"><span data-stu-id="99ffe-104">XmlType Complex Type</span></span>

<span data-ttu-id="99ffe-105">Define un fragmento XML.</span><span class="sxs-lookup"><span data-stu-id="99ffe-105">Defines an XML fragment.</span></span> <span data-ttu-id="99ffe-106">Se permite cualquier instancia de esquema; el nodo de nivel superior del fragmento debe contener un atributo de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="99ffe-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="99ffe-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ffe-107">Requirements</span></span>



| <span data-ttu-id="99ffe-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ffe-108">Requirement</span></span> | <span data-ttu-id="99ffe-109">Value</span><span class="sxs-lookup"><span data-stu-id="99ffe-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99ffe-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ffe-110">Minimum supported client</span></span><br/> | <span data-ttu-id="99ffe-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="99ffe-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99ffe-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ffe-112">Minimum supported server</span></span><br/> | <span data-ttu-id="99ffe-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="99ffe-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





