---
title: Tipo simple de UInt16Type
description: Define un tipo Short sin signo.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- UInt16Type de tipo simple de registro
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803572"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="b5d18-104">Tipo simple de UInt16Type</span><span class="sxs-lookup"><span data-stu-id="b5d18-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="b5d18-105">Define un tipo Short sin signo.</span><span class="sxs-lookup"><span data-stu-id="b5d18-105">Defines an unsigned short type.</span></span> <span data-ttu-id="b5d18-106">El valor se puede especificar como un entero de 2 bytes o como un valor hexadecimal en el intervalo comprendido entre 0 y 65.535.</span><span class="sxs-lookup"><span data-stu-id="b5d18-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="b5d18-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d18-107">Requirements</span></span>



| <span data-ttu-id="b5d18-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d18-108">Requirement</span></span> | <span data-ttu-id="b5d18-109">Value</span><span class="sxs-lookup"><span data-stu-id="b5d18-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5d18-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5d18-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d18-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b5d18-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5d18-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5d18-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d18-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5d18-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





