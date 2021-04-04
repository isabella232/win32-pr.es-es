---
description: Define un tipo de identificador único global, en formato de registro.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo simple de GUIDType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909717"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="9d117-103">Tipo simple de GUIDType (contadores de rendimiento)</span><span class="sxs-lookup"><span data-stu-id="9d117-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="9d117-104">Define un tipo de identificador único global, en formato de registro.</span><span class="sxs-lookup"><span data-stu-id="9d117-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9d117-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="9d117-105">Patterns</span></span>

<span data-ttu-id="9d117-106">El tipo simple **GUIDType** es **xs: String** , que está restringido por el patrón siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d117-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="9d117-107">El valor debe ser un tipo de identificador único global en el formato del registro.</span><span class="sxs-lookup"><span data-stu-id="9d117-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="9d117-108">Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="9d117-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="9d117-109">Utilice GUIDGen.exe o UUIDGen.exe para crear un GUID.</span><span class="sxs-lookup"><span data-stu-id="9d117-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d117-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d117-110">Requirements</span></span>



| <span data-ttu-id="9d117-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d117-111">Requirement</span></span> | <span data-ttu-id="9d117-112">Value</span><span class="sxs-lookup"><span data-stu-id="9d117-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d117-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d117-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9d117-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9d117-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d117-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d117-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9d117-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d117-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




