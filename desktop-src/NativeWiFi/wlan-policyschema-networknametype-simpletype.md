---
description: Define un tipo de cadena para los identificadores de conjunto de servicios (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Tipo simple de networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002770"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="16ee9-103">Tipo simple de networkNameType</span><span class="sxs-lookup"><span data-stu-id="16ee9-103">networkNameType Simple Type</span></span>

<span data-ttu-id="16ee9-104">El tipo simple networkNameType define un tipo de cadena para los identificadores de conjunto de servicios (SSID).</span><span class="sxs-lookup"><span data-stu-id="16ee9-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="16ee9-105">Un SSID es una cadena que tiene al menos un carácter de longitud y 32 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="16ee9-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="16ee9-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16ee9-106">Requirements</span></span>



| <span data-ttu-id="16ee9-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="16ee9-107">Requirement</span></span> | <span data-ttu-id="16ee9-108">Value</span><span class="sxs-lookup"><span data-stu-id="16ee9-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16ee9-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16ee9-109">Minimum supported client</span></span><br/> | <span data-ttu-id="16ee9-110">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16ee9-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16ee9-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16ee9-111">Minimum supported server</span></span><br/> | <span data-ttu-id="16ee9-112">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="16ee9-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




