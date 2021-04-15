---
title: Tipo simple de nonEmptyStringType
description: Define los valores utilizados para una cadena de texto que no está vacía.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Programador de tareas de tipo simple nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422438"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="d840b-104">Tipo simple de nonEmptyStringType</span><span class="sxs-lookup"><span data-stu-id="d840b-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="d840b-105">Define los valores utilizados para una cadena de texto que no está vacía.</span><span class="sxs-lookup"><span data-stu-id="d840b-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="d840b-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="d840b-106">Enumeration values</span></span>

<span data-ttu-id="d840b-107">El tipo simple **nonEmptyString** define el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="d840b-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="d840b-108">Value</span><span class="sxs-lookup"><span data-stu-id="d840b-108">Value</span></span> | <span data-ttu-id="d840b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d840b-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="d840b-110">1</span><span class="sxs-lookup"><span data-stu-id="d840b-110">1</span></span>     | <span data-ttu-id="d840b-111">La cadena contiene al menos un carácter.</span><span class="sxs-lookup"><span data-stu-id="d840b-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d840b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d840b-112">Requirements</span></span>



| <span data-ttu-id="d840b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d840b-113">Requirement</span></span> | <span data-ttu-id="d840b-114">Value</span><span class="sxs-lookup"><span data-stu-id="d840b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d840b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d840b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d840b-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d840b-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d840b-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d840b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d840b-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d840b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





