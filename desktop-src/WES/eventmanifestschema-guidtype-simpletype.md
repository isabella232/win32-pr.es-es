---
title: Tipo simple GUIDType (esquema EventManifest)
description: Define un tipo de identificador único global, en formato de registro. | Tipo simple GUIDType (esquema EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- GUIDType de tipo simple de registro
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698172"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a><span data-ttu-id="581ce-105">Tipo simple GUIDType (esquema EventManifest)</span><span class="sxs-lookup"><span data-stu-id="581ce-105">GUIDType Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="581ce-106">Define un tipo de identificador único global, en formato de registro.</span><span class="sxs-lookup"><span data-stu-id="581ce-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="581ce-107">Patrones</span><span class="sxs-lookup"><span data-stu-id="581ce-107">Patterns</span></span>

<span data-ttu-id="581ce-108">El tipo simple **GUIDType** es una cadena restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="581ce-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="581ce-109">El valor debe ser un tipo de identificador único global en el formato del registro.</span><span class="sxs-lookup"><span data-stu-id="581ce-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="581ce-110">Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="581ce-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="581ce-111">Utilice GUIDGen.exe o UUIDGen.exe para crear un GUID.</span><span class="sxs-lookup"><span data-stu-id="581ce-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="581ce-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581ce-112">Requirements</span></span>



| <span data-ttu-id="581ce-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="581ce-113">Requirement</span></span> | <span data-ttu-id="581ce-114">Value</span><span class="sxs-lookup"><span data-stu-id="581ce-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="581ce-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="581ce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="581ce-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="581ce-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="581ce-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="581ce-117">Minimum supported server</span></span><br/> | <span data-ttu-id="581ce-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="581ce-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





