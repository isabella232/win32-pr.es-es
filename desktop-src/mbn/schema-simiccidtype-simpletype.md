---
description: Define un tipo para el elemento SimIccID del perfil de banda ancha móvil.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simple de simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666503"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="c10cf-103">Tipo simple de simIccIDType</span><span class="sxs-lookup"><span data-stu-id="c10cf-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="c10cf-104">El tipo simple **simIccIDType** define un tipo para el elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) del perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="c10cf-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="c10cf-105">Este tipo es una colección de dígitos y/o letras mayúsculas y minúsculas, al menos un carácter de longitud y 20 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="c10cf-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="c10cf-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="c10cf-106">Patterns</span></span>

<span data-ttu-id="c10cf-107">El tipo simple **simIccIDType** es un token que está restringido por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="c10cf-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="c10cf-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c10cf-108">Requirements</span></span>



| <span data-ttu-id="c10cf-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10cf-109">Requirement</span></span> | <span data-ttu-id="c10cf-110">Value</span><span class="sxs-lookup"><span data-stu-id="c10cf-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c10cf-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c10cf-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c10cf-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c10cf-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c10cf-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c10cf-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c10cf-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c10cf-114">None supported</span></span><br/>                         |



 

 




