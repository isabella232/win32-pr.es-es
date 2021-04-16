---
description: Define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN inalámbrica.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo simple de nameType (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678391"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="3fcd1-103">Tipo simple de nameType (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="3fcd1-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="3fcd1-104">El tipo simple nameType define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="3fcd1-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="3fcd1-105">Los nombres y las descripciones son cadenas que tienen al menos un carácter de longitud y una longitud máxima de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fcd1-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="3fcd1-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fcd1-106">Requirements</span></span>



| <span data-ttu-id="3fcd1-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fcd1-107">Requirement</span></span> | <span data-ttu-id="3fcd1-108">Value</span><span class="sxs-lookup"><span data-stu-id="3fcd1-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fcd1-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fcd1-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3fcd1-110">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3fcd1-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3fcd1-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fcd1-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3fcd1-112">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fcd1-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




