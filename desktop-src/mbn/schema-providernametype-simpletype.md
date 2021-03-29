---
description: Define un tipo de cadena para el elemento ProviderName en el perfil de banda ancha móvil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo simple de providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541387"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="f861d-103">Tipo simple de providerNameType</span><span class="sxs-lookup"><span data-stu-id="f861d-103">providerNameType Simple Type</span></span>

<span data-ttu-id="f861d-104">El tipo simple **providerNameType** define un tipo de cadena para el elemento [**providerName**](schema-providername-providertype-element.md) en el perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="f861d-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="f861d-105">Esta cadena tiene al menos un carácter de longitud y 20 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="f861d-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="f861d-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f861d-106">Requirements</span></span>



| <span data-ttu-id="f861d-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="f861d-107">Requirement</span></span> | <span data-ttu-id="f861d-108">Value</span><span class="sxs-lookup"><span data-stu-id="f861d-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f861d-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f861d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="f861d-110">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f861d-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f861d-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f861d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="f861d-112">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f861d-112">None supported</span></span><br/>                         |



 

 




