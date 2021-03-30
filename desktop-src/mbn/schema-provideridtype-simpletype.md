---
description: Define un tipo para el elemento ProviderID del perfil de banda ancha móvil.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo simple de providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154191"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="2c052-103">Tipo simple de providerIdType</span><span class="sxs-lookup"><span data-stu-id="2c052-103">providerIdType Simple Type</span></span>

<span data-ttu-id="2c052-104">El tipo simple **providerIdType** define un tipo para el elemento [**ProviderID**](schema-providerid-providertype-element.md) del perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="2c052-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="2c052-105">Este tipo es una colección de dígitos de al menos un dígito de longitud y de 6 dígitos como máximo.</span><span class="sxs-lookup"><span data-stu-id="2c052-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="2c052-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="2c052-106">Patterns</span></span>

<span data-ttu-id="2c052-107">El tipo simple **providerIdType** es un token que está restringido por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="2c052-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="2c052-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c052-108">Requirements</span></span>



| <span data-ttu-id="2c052-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c052-109">Requirement</span></span> | <span data-ttu-id="2c052-110">Value</span><span class="sxs-lookup"><span data-stu-id="2c052-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2c052-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c052-111">Minimum supported client</span></span><br/> | <span data-ttu-id="2c052-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="2c052-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2c052-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c052-113">Minimum supported server</span></span><br/> | <span data-ttu-id="2c052-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2c052-114">None supported</span></span><br/>                         |



 

 




