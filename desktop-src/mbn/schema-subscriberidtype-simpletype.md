---
description: Define un tipo para el elemento SubscriberID del perfil de banda ancha móvil.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo simple de subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082097"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="d1ccc-103">Tipo simple de subscriberIdType</span><span class="sxs-lookup"><span data-stu-id="d1ccc-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="d1ccc-104">El tipo simple **subscriberIdType** define un tipo para el elemento [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) del perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="d1ccc-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="d1ccc-105">Este tipo es una colección de uno o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1ccc-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="d1ccc-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ccc-106">Requirements</span></span>



| <span data-ttu-id="d1ccc-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ccc-107">Requirement</span></span> | <span data-ttu-id="d1ccc-108">Value</span><span class="sxs-lookup"><span data-stu-id="d1ccc-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d1ccc-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1ccc-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ccc-110">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1ccc-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d1ccc-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1ccc-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ccc-112">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1ccc-112">None supported</span></span><br/>                         |



 

 




