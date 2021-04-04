---
description: Define un tipo de cadena para el elemento ICONFilePath en el perfil de banda ancha móvil.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo simple de iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154194"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="32e55-103">Tipo simple de iconFileType</span><span class="sxs-lookup"><span data-stu-id="32e55-103">iconFileType Simple Type</span></span>

<span data-ttu-id="32e55-104">El tipo simple **iconFileType** define un tipo de cadena para el elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) en el perfil de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="32e55-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="32e55-105">Esta cadena tiene al menos un carácter de longitud y una longitud máxima de 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="32e55-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="32e55-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e55-106">Requirements</span></span>



| <span data-ttu-id="32e55-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e55-107">Requirement</span></span> | <span data-ttu-id="32e55-108">Value</span><span class="sxs-lookup"><span data-stu-id="32e55-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="32e55-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e55-109">Minimum supported client</span></span><br/> | <span data-ttu-id="32e55-110">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="32e55-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="32e55-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e55-111">Minimum supported server</span></span><br/> | <span data-ttu-id="32e55-112">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="32e55-112">None supported</span></span><br/>                         |



 

 




