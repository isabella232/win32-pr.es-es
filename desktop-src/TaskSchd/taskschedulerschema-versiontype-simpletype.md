---
title: Tipo simple de versionType
description: Define un patrón que especifica una versión de una tarea.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Programador de tareas de tipo simple versionType
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359695"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="8c416-104">Tipo simple de versionType</span><span class="sxs-lookup"><span data-stu-id="8c416-104">versionType Simple Type</span></span>

<span data-ttu-id="8c416-105">Define un patrón que especifica una versión de una tarea.</span><span class="sxs-lookup"><span data-stu-id="8c416-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="8c416-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="8c416-106">Patterns</span></span>

<span data-ttu-id="8c416-107">El tipo simple **versionType** es una **cadena** restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="8c416-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="8c416-108">Un valor de tipo Double seguido de uno, dos o tres valores double.</span><span class="sxs-lookup"><span data-stu-id="8c416-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="8c416-109">Por ejemplo, 1,2 o 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="8c416-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c416-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c416-110">Requirements</span></span>



| <span data-ttu-id="8c416-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c416-111">Requirement</span></span> | <span data-ttu-id="8c416-112">Value</span><span class="sxs-lookup"><span data-stu-id="8c416-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c416-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c416-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8c416-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c416-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c416-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c416-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8c416-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c416-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





