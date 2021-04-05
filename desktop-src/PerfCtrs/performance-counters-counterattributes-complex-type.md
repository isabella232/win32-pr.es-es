---
description: Define una lista que contiene hasta cinco atributos de contador.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Atributo de tipo complejo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001970"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="5ff72-103">Atributo de tipo complejo</span><span class="sxs-lookup"><span data-stu-id="5ff72-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="5ff72-104">Define una lista que contiene hasta cinco atributos de contador.</span><span class="sxs-lookup"><span data-stu-id="5ff72-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5ff72-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5ff72-105">Child elements</span></span>



| <span data-ttu-id="5ff72-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ff72-106">Element</span></span>              | <span data-ttu-id="5ff72-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ff72-107">Type</span></span>                                                                               | <span data-ttu-id="5ff72-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ff72-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff72-109">**Atributo contraattribute**</span><span class="sxs-lookup"><span data-stu-id="5ff72-109">**counterAttribute**</span></span> | [<span data-ttu-id="5ff72-110">**Man: contraattribute**</span><span class="sxs-lookup"><span data-stu-id="5ff72-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="5ff72-111">Un atributo Counter que especifica cómo se muestran los datos de contador en una aplicación de consumidor.</span><span class="sxs-lookup"><span data-stu-id="5ff72-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5ff72-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ff72-112">Requirements</span></span>



| <span data-ttu-id="5ff72-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff72-113">Requirement</span></span> | <span data-ttu-id="5ff72-114">Value</span><span class="sxs-lookup"><span data-stu-id="5ff72-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ff72-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ff72-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff72-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ff72-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ff72-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ff72-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff72-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ff72-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




