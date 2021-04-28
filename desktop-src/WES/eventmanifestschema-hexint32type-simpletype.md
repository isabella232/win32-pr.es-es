---
title: Tipo simple UInt32Type (registro de eventos de Windows)
description: 'Tipo simple UInt32Type (registro de eventos de Windows): define un tipo entero sin signo.'
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Tipo simple EventLog de UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090573"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="469d7-104">Tipo simple UInt32Type (registro de eventos de Windows)</span><span class="sxs-lookup"><span data-stu-id="469d7-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="469d7-105">Define un tipo entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="469d7-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="469d7-106">El valor se puede especificar como un entero de 4 bytes o un valor hexadecimal en el intervalo comprendido entre 0 y 4.294.967.295.</span><span class="sxs-lookup"><span data-stu-id="469d7-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="469d7-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="469d7-107">Requirements</span></span>



| <span data-ttu-id="469d7-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="469d7-108">Requirement</span></span> | <span data-ttu-id="469d7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="469d7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="469d7-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="469d7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="469d7-111">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="469d7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="469d7-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="469d7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="469d7-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="469d7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





