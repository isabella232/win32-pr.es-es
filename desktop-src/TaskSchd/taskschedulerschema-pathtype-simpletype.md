---
title: Tipo simple de pathType
description: Define el número mínimo y máximo de caracteres de una cadena que define una ruta de acceso de archivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Programador de tareas de tipo simple pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686225"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="12bfb-104">Tipo simple de pathType</span><span class="sxs-lookup"><span data-stu-id="12bfb-104">pathType Simple Type</span></span>

<span data-ttu-id="12bfb-105">Define el número mínimo y máximo de caracteres de una cadena que define una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="12bfb-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="12bfb-106">La ruta de acceso no puede ser una cadena vacía y debe tener menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="12bfb-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="12bfb-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12bfb-107">Requirements</span></span>



| <span data-ttu-id="12bfb-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bfb-108">Requirement</span></span> | <span data-ttu-id="12bfb-109">Value</span><span class="sxs-lookup"><span data-stu-id="12bfb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12bfb-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12bfb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="12bfb-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12bfb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12bfb-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12bfb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="12bfb-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12bfb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





