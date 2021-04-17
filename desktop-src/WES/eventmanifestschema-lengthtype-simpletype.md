---
title: Tipo simple de LengthType
description: Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LengthType de tipo simple de registro
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359839"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="23045-104">Tipo simple de LengthType</span><span class="sxs-lookup"><span data-stu-id="23045-104">LengthType Simple Type</span></span>

<span data-ttu-id="23045-105">Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="23045-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="23045-106">El valor se puede especificar como un valor XS: unsignedShort o como una cadena que hace referencia al nombre del nodo elemento de datos que contiene el valor Short sin signo.</span><span class="sxs-lookup"><span data-stu-id="23045-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="23045-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23045-107">Requirements</span></span>



| <span data-ttu-id="23045-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="23045-108">Requirement</span></span> | <span data-ttu-id="23045-109">Value</span><span class="sxs-lookup"><span data-stu-id="23045-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23045-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23045-110">Minimum supported client</span></span><br/> | <span data-ttu-id="23045-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23045-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23045-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23045-112">Minimum supported server</span></span><br/> | <span data-ttu-id="23045-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="23045-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





