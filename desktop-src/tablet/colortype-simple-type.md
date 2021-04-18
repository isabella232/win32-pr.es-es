---
description: Define el tipo que se utiliza para especificar los valores válidos para el color de determinados elementos de un archivo XML de diario.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo simple de ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705446"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="e2a2e-103">Tipo simple de ColorType</span><span class="sxs-lookup"><span data-stu-id="e2a2e-103">ColorType Simple Type</span></span>

<span data-ttu-id="e2a2e-104">Define el tipo que se utiliza para especificar los valores válidos para el color de determinados elementos de un archivo XML de diario.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="e2a2e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2a2e-105">Remarks</span></span>

<span data-ttu-id="e2a2e-106">Un color puede ser un valor RGB hexadecimal con el formato \# RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="e2a2e-107">Debe coincidir con la siguiente expresión regular: \# \[ 0-9 – FA-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="e2a2e-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="e2a2e-108">Por ejemplo: " \# 4a79B5".</span><span class="sxs-lookup"><span data-stu-id="e2a2e-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a2e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a2e-109">Requirements</span></span>



| <span data-ttu-id="e2a2e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a2e-110">Requirement</span></span> | <span data-ttu-id="e2a2e-111">Value</span><span class="sxs-lookup"><span data-stu-id="e2a2e-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e2a2e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2a2e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a2e-113">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e2a2e-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e2a2e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2a2e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a2e-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e2a2e-115">None supported</span></span><br/>                                     |



 

 




