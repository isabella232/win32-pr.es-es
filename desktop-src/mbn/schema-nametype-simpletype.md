---
description: Define un tipo de cadena para el perfil de banda ancha móvil.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo simple de nameType (banda ancha móvil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666509"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="ee402-103">tipo simple de nameType (banda ancha móvil)</span><span class="sxs-lookup"><span data-stu-id="ee402-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="ee402-104">El tipo simple **nameType** define un tipo de cadena para el perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="ee402-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="ee402-105">Esta cadena tiene al menos un carácter de longitud y una longitud máxima de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee402-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
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

## <a name="requirements"></a><span data-ttu-id="ee402-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee402-106">Requirements</span></span>



| <span data-ttu-id="ee402-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee402-107">Requirement</span></span> | <span data-ttu-id="ee402-108">Value</span><span class="sxs-lookup"><span data-stu-id="ee402-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ee402-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee402-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ee402-110">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ee402-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ee402-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee402-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ee402-112">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee402-112">None supported</span></span><br/>                         |



 

 




