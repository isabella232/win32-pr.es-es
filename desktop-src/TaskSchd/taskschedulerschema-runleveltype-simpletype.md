---
title: Tipo simple de runLevelType
description: Define los valores posibles para el elemento nivel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Programador de tareas de tipo simple runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676877"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="ed426-104">Tipo simple de runLevelType</span><span class="sxs-lookup"><span data-stu-id="ed426-104">runLevelType Simple Type</span></span>

<span data-ttu-id="ed426-105">Define los valores posibles para el elemento [**nivel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed426-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="ed426-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="ed426-106">Enumeration values</span></span>

<span data-ttu-id="ed426-107">El tipo simple **runLevelType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ed426-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="ed426-108">Value</span><span class="sxs-lookup"><span data-stu-id="ed426-108">Value</span></span>            | <span data-ttu-id="ed426-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed426-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="ed426-110">LeastPrivilege</span><span class="sxs-lookup"><span data-stu-id="ed426-110">LeastPrivilege</span></span>   | <span data-ttu-id="ed426-111">Las tareas se ejecutan con los privilegios mínimos (LUA).</span><span class="sxs-lookup"><span data-stu-id="ed426-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="ed426-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="ed426-112">HighestAvailable</span></span> | <span data-ttu-id="ed426-113">Las tareas se ejecutan con los privilegios más altos.</span><span class="sxs-lookup"><span data-stu-id="ed426-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="ed426-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed426-114">Requirements</span></span>



| <span data-ttu-id="ed426-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed426-115">Requirement</span></span> | <span data-ttu-id="ed426-116">Value</span><span class="sxs-lookup"><span data-stu-id="ed426-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed426-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed426-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ed426-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed426-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed426-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed426-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ed426-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed426-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





